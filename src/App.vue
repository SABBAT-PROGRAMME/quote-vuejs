<!-- Tample -->
<template>
  <div class="container">
    <article class="card p-5">
      <h3><span>« </span>{{ quotes[index].quote }} <span>»</span></h3>
      <hr />
      <b></b>
      <p>{{ quotes[index].author }}</p>
      <div class="buttons">
        <button @click="change">Suivant</button>
      </div>
    </article>
  </div>
  <div></div>
</template>

<!-- Script -->
<script setup>
import { ref } from "vue";
const quotes = ref([
  {
    author: "Albert Einstein",
    quote:
      "La vie, c'est comme une bicyclette, il faut avancer pour ne pas perdre l'équilibre.",
  },
  {
    author: "Marie Curie",
    quote: "Rien dans la vie n'est à craindre, tout est à comprendre.",
  },
  {
    author: "Confucius",
    quote: "Une petite impatience ruine un grand projet.",
  },
  {
    author: "Nelson Mandela",
    quote: "Cela semble toujours impossible, jusqu'à ce qu'on le fasse.",
  },
  {
    author: "Victor Hugo",
    quote: "La liberté commence où l'ignorance finit.",
  },
  {
    author: "Mahatma Gandhi",
    quote:
      "La force ne vient pas des capacités physiques, elle vient d'une volonté indomptable.",
  },
  {
    author: "René Descartes",
    quote: "Je pense, donc je suis.",
  },
  {
    author: "Lao Tseu",
    quote: "Un voyage de mille lieues commence toujours par un premier pas.",
  },
  {
    author: "Walt Disney",
    quote:
      "Tous nos rêves peuvent devenir réalité, si nous avons le courage de les poursuivre.",
  },
  {
    author: "Socrate",
    quote: "La seule chose que je sais, c'est que je ne sais rien.",
  },
]);

let index = ref(0);

const change = () => {
  index.value = Math.floor(Math.random() * quotes.value.length);
  console.log(index.value);
};
</script>

<!-- Style -->

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto+Mono:ital,wght@0,100..700;1,100..700&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Nerko+One&display=swap");

/* .roboto-mono-<uniquifier > {
  font-family: "Roboto Mono", monospace;
  font-optical-sizing: auto;
  font-weight: <weight>;
  font-style: normal;
} */

/* .nerko-one-regular {
  font-family: "Nerko One", cursive;
  font-weight: 400;
  font-style: normal;
} */

html,
body {
  background-color: #c6c6c6;
}
.container {
  width: 80%;
  height: 80vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(#cfd5e2, #8b49c8);
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  margin-top: 50px;
  border-radius: 5px;
}

.container:hover {
  cursor: pointer;
  background: linear-gradient(to right, #8b49c8, #cfd5e2);
}

.card {
  width: 50%;
  background-color: #fff;
  color: black;
  padding: 20px;
  font-family: "Roboto Mono", monospace;
  font-weight: 500;
  font-style: italic;
}

h3 {
  color: #0172ad;
}

span {
  font-size: 1.5em;
  font-weight: bold;
  color: gray;
}

p {
  padding-top: 10px;
  font-size: 1.4em;
  text-align: left;
  font-family: "Nerko One", cursive;
  color: grey;
}
b {
  background-color: #0172ad;
  width: 10%;
  height: 10%;
}
</style>
