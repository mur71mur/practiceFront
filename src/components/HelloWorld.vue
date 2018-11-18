<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <p>aaa</p>
    <div class="animation">
      <p>スクロールでふわっと表示させたい要素</p>
      <p>スクロールでふわっと表示させたい要素</p>
      <p>スクロールでふわっと表示させたい要素</p>
      <p>スクロールでふわっと表示させたい要素</p>
      <p>スクロールでふわっと表示させたい要素</p>
      <p>スクロールでふわっと表示させたい要素</p>
     <p>スクロールでふわっと表示させたい要素</p>
    </div>
    <ul>
      <li>
        <a
          href="https://vuejs.org"
          target="_blank"
        >
          Core Docs
        </a>
      </li>
      <li>
        <a
          href="https://forum.vuejs.org"
          target="_blank"
        >
          Forum
        </a>
      </li>
      <li>
        <a
          href="https://chat.vuejs.org"
          target="_blank"
        >
          Community Chat
        </a>
      </li>
      <li>
        <a
          href="https://twitter.com/vuejs"
          target="_blank"
        >
          Twitter
        </a>
      </li>
      <br>
      <li>
        <a
          href="http://vuejs-templates.github.io/webpack/"
          target="_blank"
        >
          Docs for This Template
        </a>
      </li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li>
        <a
          href="http://router.vuejs.org/"
          target="_blank"
        >
          vue-router
        </a>
      </li>
      <li>
        <a
          href="http://vuex.vuejs.org/"
          target="_blank"
        >
          vuex
        </a>
      </li>
      <li>
        <a
          href="http://vue-loader.vuejs.org/"
          target="_blank"
        >
          vue-loader
        </a>
      </li>
      <li>
        <a
          href="https://github.com/vuejs/awesome-vue"
          target="_blank"
        >
          awesome-vue
        </a>
      </li>
    </ul>
  </div>
</template>

<script lamg="ts">
export default {
  name: 'Hell',
  data () {
    return {
      msg: 'Welcome '
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
p {
  color: blue;
}
.fadeInDown {
 -webkit-animation-fill-mode:both;
 -ms-animation-fill-mode:both;
 animation-fill-mode:both;
 -webkit-animation-duration:1s;
 -ms-animation-duration:1s;
 animation-duration:1s;
 -webkit-animation-name: fadeInDown;
 animation-name: fadeInDown;
 visibility: visible !important;
}
@-webkit-keyframes fadeInDown {
 0% { opacity: 0; -webkit-transform: translateY(200px); }
 100% { opacity: 1; -webkit-transform: translateY(0); }
}
@keyframes fadeInDown {
 0% { opacity: 0; -webkit-transform: translateY(200px); -ms-transform: translateY(200px); transform: translateY(200px); }
 100% { opacity: 1; -webkit-transform: translateY(0); -ms-transform: translateY(0); transform: translateY(0); }
}
</style>

<script>
jQuery(function(){
jQuery('.animation').css('visibility','hidden');
jQuery(window).scroll(function(){
 var windowHeight = jQuery(window).height(),
     topWindow = jQuery(window).scrollTop();
 jQuery('.animation').each(function(){
  var targetPosition = jQuery(this).offset().top;
  if(topWindow > targetPosition - windowHeight + 100){
   jQuery(this).addClass("fadeInDown");
  }
 });
});
});

</script>
