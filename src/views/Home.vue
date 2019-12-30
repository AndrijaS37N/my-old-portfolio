<template>
  <div>
    <img
      alt="That's our pale blue dot!"
      id="earth_image"
      src="../assets/earth_pic.png"
      width="100"
      height="100"
    />
    <div class="row">
      <Message class="glow" message="Andrija Đurić" />
    </div>
    <br />
    <br />
    <h1 id="surfer_emoji">🏄🏻‍♂️</h1>
    <br />
    <div>
      <div class="row">
        <h3 class="flash">Email &#128236;</h3>
        <a target="_blank" rel="noopener noreferrer" href="mailto:andrija.djur@gmail.com">Gmail</a>
        <br />
        <br />
        <a
          target="_blank"
          rel="noopener noreferrer"
          href="mailto:andrija.djuric@protonmail.com"
        >ProtonMail</a>
      </div>
      <br />
      <div class="row">
        <h3 class="flash">💻 Engineering</h3>
        <a target="_blank" rel="noopener noreferrer" href="https://github.com/AndrijaS37N">GitHub</a>
        <br />
        <br />
        <a target="_blank" rel="noopener noreferrer" href="https://gitlab.com/AndrijaS37N">GitLab</a>
        <br />
        <br />
        <a
          target="_blank"
          rel="noopener noreferrer"
          href="https://www.linkedin.com/in/andrijadjuric/"
        >LinkedIn</a>
        <br />
        <br />
      </div>
      <br />
      <div class="row">
        <h3 class="flash">Social 🎭</h3>
        <a target="_blank" rel="noopener noreferrer" href="https://twitter.com/anakalewe">Twitter</a>
        <br />
        <br />
        <a
          target="_blank"
          rel="noopener noreferrer"
          href="https://www.facebook.com/andrija.djuric"
        >Facebook</a>
        <br />
        <br />
        <a
          target="_blank"
          rel="noopener noreferrer"
          href="https://www.instagram.com/anakalewe/"
        >Instagram</a>
        <br />
        <br />
        <a
          target="_blank"
          rel="noopener noreferrer"
          href="https://soundcloud.com/andrija-djuric"
        >SoundCloud</a>
        <br />
        <br />
        <a target="_blank" rel="noopener noreferrer" href="https://linktr.ee/anakalewe">Linktree</a>
      </div>
      <br />
      <div class="row">
        <h3 class="flash">🎨 Art</h3>
        <a
          target="_blank"
          rel="noopener noreferrer"
          href="https://myalbum.com/album/NipdVu7uWTZe"
        >Seaworthy MyAlbum.com</a>
        <br />
        <br />
        <a
          target="_blank"
          rel="noopener noreferrer"
          href="https://myalbum.com/album/DFszpyEyQuDp"
        >February Getaway 2018 MyAlbum.com</a>
        <br />
        <br />
        <a
          target="_blank"
          rel="noopener noreferrer"
          href="https://myalbum.com/album/Tn00FYCQ025f"
        >February Getaway 2019 MyAlbum.com</a>
        <br />
        <br />
        <a target="_blank" rel="noopener noreferrer" href="https://500px.com/andrijas37n">500px</a>
        <br />
        <br />
        <a
          target="_blank"
          rel="noopener noreferrer"
          href="https://www.youtube.com/channel/UCyaIpfAjsJFhbHM55_7tOeQ"
        >YouTube</a>
        <br />
        <br />
        <a
          target="_blank"
          rel="noopener noreferrer"
          href="https://poetizer.com/poem/106749"
        >Galeb Poetizer</a>
        <br />
        <br />
        <a
          target="_blank"
          rel="noopener noreferrer"
          href="https://poetizer.com/poem/106618"
        >Winds of Winter Poetizer</a>
        <br />
        <br />
        <a
          target="_blank"
          rel="noopener noreferrer"
          href="https://poetizer.com/poem/106705"
        >Eärendil the Mariner Poetizer</a>
      </div>
      <br />
    </div>
  </div>
</template>

<script scoped lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Message from "@/components/Message.vue"; /// @ is an alias to /src

@Component({
  components: {
    Message
  }
})
export default class Home extends Vue {}
</script>

<style lang="css">
a {
  font-size: 30px;
  font-weight: lighter;
  transition: background 1s, color 1s;
  -webkit-transition: background 1s, color 1s;
  margin: 20px 0px 20px 0px;
  color: #7ba1c7;
}
a:hover {
  color: #bfd9f3;
}
h3 {
  margin: 25px 0px 10px 0px;
  font-size: 42px;
}
.row {
  margin-bottom: 18px;
  margin-top: 0px;
  margin-left: 20px;
  margin-right: 20px;
}
.row a {
  text-decoration: none;
  border-bottom: 2px solid;
}
.glow {
  color: #fff;
  text-align: center;
  -webkit-animation: glow 1.2s ease-in-out infinite alternate;
  -moz-animation: glow 1.2s ease-in-out infinite alternate;
  animation: glow 1.2s ease-in-out infinite alternate;
}
#earth_image {
  -webkit-filter: drop-shadow(0 0 10px rgb(255, 255, 255, 0.85));
  filter: drop-shadow(0 0 10px rgb(255, 255, 255, 0.85));
  animation: spin 7s infinite linear;
}
#surfer_emoji {
  -webkit-animation: mover 1.2s infinite alternate;
  animation: surfer_swing 1.2s infinite alternate;
  margin-top: -40px;
  margin-bottom: 0px;
  font-size: 55px;
}
@-webkit-keyframes surfer_swing {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(-10px);
  }
}
@keyframes surfer_swing {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(-10px);
  }
}
@keyframes glow {
  to {
    text-shadow: 0 0 40px #fff;
  }
}
@keyframes spin {
  to {
    transform: rotate(360deg);
  }
}
</style>