<script>
export default {
  data() {
    return {
      message: "hello world!",
      show: true,
      color: "green",
    };
  },
  methods: {
    ReverseMessage() {
      this.message = this.message.split("").reverse().join("");
    },
    notify() {
      alert("this is notify");
    },
    toggleColor() {
      this.color = this.color === "green" ? "blue" : "green";
    },
  },
};
</script>

<template>
  <div :class="color" class="card">
    <h1>{{ message }}</h1>
    <p>
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsum obcaecati,
      id, quas sunt modi harum veritatis impedit consequuntur ipsa totam
      corporis facilis consequatur libero, natus sed sint facere? Labore, nihil!
    </p>
    <button @click="ReverseMessage" >Reverse message</button>
    <button @click="message += '!'">Append "!"</button>
    <button @click="toggleColor" >change color</button>
    <a href="https://vuejs.org" @click.prevent="notify">
      A link with e.preventDefault()
    </a>
  </div>
</template>

<style>

</style>