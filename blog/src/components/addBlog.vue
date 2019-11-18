<template>
  <div id="add-blog">
    <h2>Add a new blog post</h2>
    <form>
      <label for>Blog title</label>
      <input type="text" v-model.lazy="blog.title" required />
      <label for>Blog content</label>
      <textarea v-model.lazy="blog.content"></textarea>
      <div id="checkboxes">
        <label for>Ninjas</label>
        <input type="checkbox" value="ninjas" v-model="blog.categories" />
        <label for>Wizards</label>
        <input type="checkbox" value="wizards" v-model="blog.categories" />
        <label for>Mario</label>
        <input type="checkbox" value="mario" v-model="blog.categories" />
        <label for>Cheese</label>
        <input type="checkbox" value="cheese" v-model="blog.categories" />
      </div>
      <label for="">Author</label>
      <select v-model="blog.author">
        <option v-for="author in authors">{{author}}</option>
      </select>
    </form>

    <div id="preview">
      <h3>Preview BLog</h3>
      <p>blog title: {{blog.title}}</p>
      <p>blog content: {{blog.content}}</p>
      <p>blog categories</p>
      <ul>
        <li v-for="cat in blog.categories">{{cat}}</li>
      </ul>
      <p>author: {{blog.author}}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      blog: {
        title: "",
        content: "",
        categories: [],
        author:''
      },
      authors: ['ahmad','ghaith','abdool']
    };
  },
  methods: {}
};
</script>

<style lang="scss">
#add-blog {
  margin: 20px auto;
  max-width: 500px;
}

label {
  display: block;
  margin: 20px 0 10px;
}

input[type="text"],
textarea {
  display: block;
  width: 100%;
}
#preview {
  padding: 10px 20px;
  border: 1px dotted #ccc;
  margin: 30px 0;
}
h3 {
  margin-top: 10px;
}

#checkboxes input {
  display: inline-block;
  margin-right: 10px;
}

#checkboxes label {
  display: inline-block;
}
</style>
