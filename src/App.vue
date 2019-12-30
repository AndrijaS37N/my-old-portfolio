<template>
  <div id="app">
    <div class="stars small"></div>
    <div class="stars medium"></div>
    <div class="stars large"></div>
    <div id="nav">
      <div>
        <router-link to="/">Home</router-link>
        <br />
        <router-link to="/about">About</router-link>
      </div>
    </div>
    <div>
      <transition name="fade" mode="out-in" v-on:after-enter="afterEnter" appear>
        <router-view>
          <i class="fas fa-truck-loading"></i>
        </router-view>
      </transition>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  methods: {
    afterEnter: function() {
      console.log("Log: Page transition.");
    }
  }
});
</script>

<style lang="scss">
p {
  font-size: 30px;
}
h1 {
  text-align: center;
  margin-top: 6px;
  margin-bottom: 20px;
  font-weight: 200;
  font-size: 60px;
}
html {
  @import url("https://fonts.googleapis.com/css?family=Muli");
  font-family: "Muli", sans-serif;
  background: -webkit-linear-gradient(#eee, rgba(0, 0, 0, 0) 0%),
    -webkit-linear-gradient(-45deg, #080c46 43.5%, #020119 0%);
  background-attachment: fixed;
  height: 100%;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.35s;
}
.fade-enter,
.fade-leave-active {
  opacity: 0;
}
.flash {
  animation-name: flash;
  animation-duration: 1.2s;
  animation-timing-function: linear;
  animation-iteration-count: infinite;
  animation-direction: alternate;
  animation-play-state: running;
  font-weight: lighter;
}
#app {
  text-align: center;
  color: #618ab3;
  overflow-x: hidden;
}
#nav {
  padding: 8px 0 20px 0;
  a {
    padding-left: 10px;
    padding-right: 10px;
    font-size: 40px;
    text-transform: lowercase;
    text-decoration: none;
    color: #42b98393;
    &.router-link-exact-active {
      color: #42b983ec;
    }
    transition: background 1.2s, color 1.2s;
    -webkit-transition: background 1.2s, color 1.2s;
  }
  a:hover {
    color: rgb(198, 244, 205);
  }
}
@keyframes flash {
  from {
    color: #c7dcf2;
  }
  to {
    color: #618ab3;
  }
}
</style>

<style scoped lang="scss">
body {
  height: 100%;
  width: 100%;
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}
/*
Note: A warning pops up when compiling -> a non-string value, to unquote()
will be an error in future versions of Sass. Not really sure what this warning is all about.
*/
@function box-shadow($stars) {
  $box_shadow: ();
  @for $i from 1 to $stars {
    $box_shadow: append(
      $box_shadow,
      (random(2000) + 0px) (random(2000) + 0px) #fff,
      comma
    );
  }
  @return unquote($box_shadow);
}
// Note: Memory intensive. Star boxes are here.
$box_shadow_large: box-shadow(50);
$box_shadow_medium: box-shadow(80);
$box_shadow_small: box-shadow(240);
.stars.large {
  height: 3px;
  width: 3px;
  background: transparent;
  box-shadow: $box_shadow_large;
  animation: slide_large linear 30s infinite;
}
.stars.medium {
  height: 2px;
  width: 2px;
  background: transparent;
  box-shadow: $box_shadow_medium;
  animation: slide_medium linear 30s infinite;
}
.stars.small {
  height: 1px;
  width: 1px;
  background: transparent;
  box-shadow: $box_shadow_small;
  animation: blink_small 2.4s infinite;
}
@keyframes slide_large {
  0% {
    $colors: "#fff", "transparent";
    $stars: $box_shadow_large;
    @for $i from 1 to length($stars) + 1 {
      $star: set-nth(
        nth($stars, $i),
        3,
        unquote(nth($colors, length($colors)))
      );
      $stars: set-nth($stars, $i, $star);
    }
    box-shadow: $stars;
    transform: translate(300px, -100px);
  }
  20% {
    box-shadow: $box_shadow_large;
  }
  80% {
    box-shadow: $box_shadow_large;
  }
  100% {
    $colors: "#fff", "transparent";
    $stars: $box_shadow_large;
    @for $i from 1 to length($stars) + 1 {
      $star: set-nth(
        nth($stars, $i),
        3,
        unquote(nth($colors, length($colors)))
      );
      $stars: set-nth($stars, $i, $star);
    }
    box-shadow: $stars;
    transform: translate(-400px, 300px);
  }
}
@keyframes slide_medium {
  0% {
    $colors: "#fff", "transparent";
    $stars: $box_shadow_large;
    @for $i from 1 to length($stars) + 1 {
      $star: set-nth(
        nth($stars, $i),
        3,
        unquote(nth($colors, length($colors)))
      );
      $stars: set-nth($stars, $i, $star);
    }
    box-shadow: $stars;
    transform: translate(600px, -200px);
  }
  30% {
    box-shadow: $box_shadow_large;
  }
  90% {
    box-shadow: $box_shadow_large;
  }
  100% {
    $colors: "#fff", "transparent";
    $stars: $box_shadow_large;
    @for $i from 1 to length($stars) + 1 {
      $star: set-nth(
        nth($stars, $i),
        3,
        unquote(nth($colors, length($colors)))
      );
      $stars: set-nth($stars, $i, $star);
    }
    box-shadow: $stars;
    transform: translate(-200px, 50px);
  }
}
@keyframes blink_small {
  0% {
    box-shadow: $box_shadow_small;
  }
  70% {
    $colors: "#fff", "transparent";
    $stars: $box_shadow_small;
    @for $i from 1 to length($stars) {
      $star: set-nth(
        nth($stars, $i),
        3,
        unquote(nth($colors, random(length($colors))))
      );
      $stars: set-nth($stars, $i, $star);
    }
    box-shadow: $stars;
  }
  100% {
    box-shadow: $box_shadow_small;
  }
}
</style>