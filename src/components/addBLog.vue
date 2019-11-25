<template>
  <div id="add-blog">
    <h2>Add a New Blog POst</h2>
    <form class="blog">
      <label>Blog Title</label>
      <input type="text" v-model="blog.title" required /><br>
      <label>Blog Content</label>
      <textarea v-model="blog.content"></textarea>
    </form>
    <div id="checkboxes">
      <ul>
        <li>
          <p>Ninja</p>
          <input type="checkbox" value="ninja" v-model="blog.categories"/>
        </li>
        <li>
          <p>Wizard</p>
         <input type="checkbox" value="wiz" v-model="blog.categories"/>
        </li>
        <li>
          <p>Mario</p>
          <input type="checkbox" value="mario" v-model="blog.categories"/>
        </li>

      </ul>
    </div>
    <p>Author:</p>
    <select v-model="blog.author" >
      <option v-for="author in authors" v-bind:key="author">{{author}}</option>
    </select>


    <div id="preview">
      <h3>Preview Blog</h3>
      <p>BLog Title {{blog.title}}</p>
      <p>Blog Content {{blog.content}}</p>
      <p>Blog Categories</p>
      <ul>
        <li v-for="category in blog.categories" v-bind:key="category" >{{category}}</li>
      </ul>
      <p>Author: {{blog.author}}</p>
    </div>
  </div>



</template>



<script>
export default {
  name: 'addBLog',
  data() {
    return {
      blog:{
        title:'',
        content:'',
        categories:[],
        author:''
      },
      authors:['Haneen','Omar','Salem']
    }
  }
}

</script>


<style scoped>
#addblog{
  max-width:500px;

}

label {
  display:block;
  margin:14px 0 -9px;
 }
select{
  width:200px;
  height:30px;
}
input,textarea{
  width:500px;
  padding:8px;
  margin:40px 0 0 0;
}
#preview{
  border:1px dotted #ccc;
  width:500px;
  background-color:#eee;
  margin: 20px 388px;
}
#checkboxes input{
  display:inline-block;
  margin-right:10px;
}
#checkboxes ul li{
  display:inline-block;
  width:100px;
}
</style>
