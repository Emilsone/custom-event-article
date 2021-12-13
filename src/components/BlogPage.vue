<template>
  <section id="BlogPage">
    <h1 class="heading-text">Welcome to my Blog</h1>

    <div class="parent-container">
      <div class="Card-body">
        <BlogContent
          title="Introduction to CSS"
          content="CSS is a stylesheet language used to style the structure of our document"
          @displayData="fetchData($event)"
        />
      </div>
      <div class="Card-body">
        <BlogContent
          title="What is $Emit in Vue Js"
          content="Vue $emit is a function that lets us emit, or send, custom events "
          @displayData="fetchData($event)"
        />
      </div>
      <div class="Card-body">
        <BlogContent
          title="Understanding Currying"
          content="Currying simply means evaluating functions with multiple arguments"
          @displayData="fetchData($event)"
        />
      </div>
      
    </div>
      <h4 class="result-text">Result: {{ result }}</h4>
  </section>
</template>

<script>
import BlogContent from "../components/BlogContent.vue";
export default {
  name: "BlogPage",
  components: {
    BlogContent,
  },
  data: () => ({
    result: "",
  }),
  methods: {
    fetchData(data) {
      this.result = data;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.heading-text {
  text-align: center;
  color:black;
font-weight:bold;
font-size:30px;
}
.result-text{
  text-align: center;
  font-weight:bold;
}
.parent-container {
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 20px 0px;
}
.Card-body {
  background-color: #f8f9f8;
  color: #0c0e2d;
  padding: 40px 20px;
  margin: 40px;
  line-height: 1.9rem;
}
</style>
