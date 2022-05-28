<template>
    <section class="hero">
  <div class="content">
    <h2 id="text"></h2>
    <p>Welcome to my page. I'm on a journey to becoming the best coder and person I can be. I will use this platform to showcase my work and endeavours.</p>
    </div>
  <div class="waves"></div>
</section>


</template>

<script>
export default {
    mounted() {
        const sentences = [
  "Hi! I'm Kago.",
  "Welcome to my Portfolio/Blog page.",
  "I'm (somewhat) of a decent coder :)",
  "and I have an obsession with sports.",
  "I desire to combine my love for coding and sports into one.",
  "I'm really glad to a have you here!"
];

function waitForMs(ms) {
  return new Promise((resolve) => setTimeout(resolve, ms));
}

async function typeSentence(sentence, element, delay = 100) {
  const letters = sentence.split("");
  let i = 0;
  while (i < letters.length) {
    await waitForMs(delay);
    document.querySelector(element).append(letters[i]);
    i++;
  }
}

async function deleteSentence(element) {
  const sentence = document.querySelector(element).innerHTML;
  const letters = sentence.split("");
  while (letters.length > 0) {
    await waitForMs(100);
    letters.pop();
    document.querySelector(element).innerHTML = letters.join("");
  }
}


async function sentenceLoop(sentenceList, element) {
  let i = 0;
  while (true) {
    await typeSentence(sentenceList[i], element);
    await waitForMs(1500);
    await deleteSentence(element);
    await waitForMs(500);
    i++;
    if (i >= sentenceList.length) {
      i = 0;
    }
  }
}

sentenceLoop(sentences, "#text");

    }
}
</script>

<style scoped>
* {
    margin: 0px;
    padding: 0px;
    box-sizing: border-box;
}

.content {
  max-width: 600px;
  margin: 0 auto;
  padding: 0 20px;
}

.hero {
  position: relative;
  background: #333333;
  color: white;
  height: 40vh;
  display: flex;
  align-items: center;
  overflow: hidden;
}

.hero h2 {
  position: relative;
  z-index: 1;
  font-size: 2rem;
  margin: 0 0 10px;
  line-height: 1;
  color: rgba(255, 255, 255, 0.9);
}

.hero h2::after {
  content: "";
  width: 3px;
  height: 100%;
  background: white;
  position: absolute;
  animation: blink 1s infinite;
}

@keyframes blink {
  0%,
  49% {
    background: white;
  }
  50%,
  100% {
    background: #333333;
  }
}

.hero p {
  position: relative;
  z-index: 1;
  font-size: 1.1rem;
  color: rgba(255, 255, 255, 0.5);
  line-height: 1.4;
}

/* ========================= */

.waves {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 125px;
  background-color: white;
  box-shadow: inset 0 0 50px rgba(0, 0, 0, 0.5);
  transition: 500ms;
}

.waves::before,
.waves::after {
  content: '';
  position: absolute;
  width: 300vw;
  height: 300vw;
  top: -65vw;
  left: 50%;
  transform: translate(-50%, -75%);
}

.waves::before {
  border-radius: 44%;
  background: rgba(51, 51, 51, 1);
  animation: waves 8s linear infinite;
}

.waves::after {
  border-radius: 44%;
  background: rgba(51, 51, 51, 0.5);
  animation: waves 15s linear infinite;
}

@keyframes waves {
  0% {
    transform: translate(-50%, -75%) rotate(0deg);
  }
  
  100% {
    transform: translate(-50%, -75%) rotate(360deg);
  }
}




</style>