<template>
  <div>
    <hr id="green_hr_about" />
    <br />
    <h3 class="flash" id="h3_about">Hi</h3>
    <p id="info_about">
      <!-- Click or scroll through the text below to make it brighter. -->
      🛸
    </p>
    <div onscroll id="div_about">
      <p>
        I'm a software engineer based in Belgrade, Serbia that's currently
        looking for UI/UX development work focused on React. I've worked with a
        number of different tools and languages.
      </p>
      <h1>&#127889;</h1>
      <p>React library, CSR and SSR with the Next.js framework.</p>
      <h1>&#128247;</h1>
      <p>Vue.js with cool SCSS animations.</p>
      <h1>&#127935;</h1>
      <p>PostgreSQL, Redis, MongoDB and MySQL databases.</p>
      <h1>🐚</h1>
      <p>HTML5, CSS3 and design systems like Chakra UI.</p>
      <h1>&#9203;</h1>
      <p>ES2015+ JavaScript & TypeScript, and Node.js servers.</p>
      <h1>🍪</h1>
      <p>Jest tests and GraphQL Apollo for requesting data.</p>
      <h1>🧁</h1>
      <p>Also done C/C++, Java Spring Boot, Python, Bash.</p>
      <h1 style="font-size: 48px;">🐆 🐘 🐍</h1>
      <p>Check out my GitHub for more details on the projects I've done!</p>
      <h1 style="font-size: 32px;">🌴 🌱 🏡 🌳 🌲</h1>
      <br />
      <hr id="blue_hr_about" />
      <br />
      <br />
      <br />
      <p>
        I'm a follower of topics and trends such as AI, modern UI/UX, tech
        automation progress, graphics and game development advances,
        decentralized systems, alternative computing and brain-computer
        interfaces.
      </p>
      <p>
        <span style="color: #bfd9f3; text-decoration: none; font-weight: 900;"
          >Email me for a complete résumé.</span
        >
        I have many hobbies and passions, some of which you can check out on the
        home page in the art section.
      </p>
    </div>
    <img
      alt="That's me!"
      src="../assets/portrait_pic.jpg"
      width="120"
      height="120"
      id="image_of_me"
    />
    <br />
    <p class="flash">
      Hit me up,
      <a
        target="_blank"
        rel="noopener noreferrer"
        href="mailto:andrija.djur@gmail.com"
        id="lets_talk"
        >let's talk.</a
      >
      <img
        alt="Let's talk!"
        src="../assets/call_gesture_pic.png"
        width="30"
        height="30"
        id="call_me_logo"
      />
    </p>
    <br />
  </div>
</template>

<script>
import $ from "jquery";

export default {
  name: "welcome",
  mounted: function() {
    $(document).ready(function() {
      $(window).scroll(function() {
        // check if scroll event happened
        if ($(document).scrollTop() > 25) {
          // check if user scrolled more than 25 from top of the browser window
          $("#div_about").css("color", "#bfd9f3");
        } else {
          $("#div_about").css("color", "#618ab3"); // color hash from App.vue
        }
      });
    });
  },
};
</script>

<style lang="css">
p {
  font-size: 28px;
  margin: 0px 20px 34px 20px;
  transition: background 1s, color 1s;
  -webkit-transition: background 1s, color 1s;
}
p a {
  text-decoration: none;
  border-bottom: 2px solid;
}
#lets_talk {
  font-weight: lighter;
  font-size: 25px;
}
#h3_about {
  margin-top: 14px;
  margin-bottom: 8px;
}
#image_of_me {
  border-radius: 100px;
}
#info_about {
  font-size: 5rem;
  position: absolute;
  margin-left: auto;
  margin-right: auto;
  left: 0;
  right: 0;
  top: 85rem;
  text-align: center;
  opacity: 0;
  animation-name: top_fade_out;
  animation-duration: 7s;
  color: #42b983ec;
}
#green_hr_about {
  max-width: 50px;
  color: #42b98393;
  border-color: #42b98393;
  width: 50px;
}
#blue_hr_about {
  max-width: 100px;
  color: #7ba1c7;
  border-color: #7ba1c7;
  width: 100px;
}
#call_me_logo {
  margin-top: 5px;
}
@keyframes top_fade_out {
  0% {
    top: -3rem;
    opacity: 0;
  }
  10% {
    right: 70%;
    opacity: 0.8;
  }
  20% {
    top: 20%;
    left: 30%;
    opacity: 1;
  }
  40% {
    top: 35%;
    right: 80%;
    opacity: 1;
  }
  60% {
    top: 53%;
    left: 70%;
    opacity: 1;
  }
  76% {
    top: 67%;
    opacity: 1;
  }
  80% {
    top: 73%;
    opacity: 1;
  }
  84% {
    top: 80%;
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}
</style>
