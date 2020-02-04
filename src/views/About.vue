<template>
  <div>
    <hr id="green_hr_about" />
    <br />
    <h3 class="flash" id="h3_about">Hi</h3>
    <p id="info_about">
      <!-- Click or scroll through the text below to make it brighter. -->
      🛸
    </p>
    <div onclick id="div_about">
      <p>I'm a software engineer based in Belgrade, Serbia that's currently working as a blockchain developer. I've worked with a number of different technologies.</p>
      <h1>&#127889;</h1>
      <p>C and C++ programming languages.</p>
      <h1>&#128247;</h1>
      <p>Node, React and Vue JavaScript giants.</p>
      <h1>&#127935;</h1>
      <p>Java Spring Boot framework with Maven and MySQL.</p>
      <h1>🐚</h1>
      <p>Python scripting for processing files and data.</p>
      <h1>&#9203;</h1>
      <p>SDLC and UML systems design.</p>
      <h1>🍪</h1>
      <p>Ethers.js and Solidity.</p>
      <h1>🔑</h1>
      <br />
      <hr id="blue_hr_about" />
      <br />
      <br />
      <br />
      <p>Also, I'm a follower of topics and trends such as AI, high-performance computing, automation, game development, decentralized systems, alternative computing and brain-computer interfaces.</p>
      <p>Email me for a complete résumé. I have many hobbies, some of which you can check out on the home page in the art section.</p>
    </div>
    <img alt="That's me!" src="../assets/portrait_pic.jpg" width="120" height="120" id="image_of_me" />
    <br />
    <p class="flash">
      Hit me up,
      <a
        target="_blank"
        rel="noopener noreferrer"
        href="mailto:andrija.djur@gmail.com"
        id="lets_talk"
      >let's talk.</a>
      <img alt="Let's talk!" src="../assets/call_gesture_pic.png" width="30" height="30" id="call_me_logo" />
    </p>
    <br />
  </div>
</template>

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
#div_about:hover {
  color: #bfd9f3;
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