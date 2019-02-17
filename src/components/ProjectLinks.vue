<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      Welcome to my home page. In case you are interested in one of my projects please click the links below.
    </p>
    <h3>My projects:</h3>
    <ul>
      <li>
        <a href="https://stringtools.netlify.com">String Tools (Vue)</a>
      </li>
      <li>
        <a href="https://avatar-generator.netlify.com">Avatar Generator (Vue) - Nov 2018</a>
      </li>
      <li>
        <a href="https://webxslt.netlify.com/">Web XSLT processor (React+Bootstrap) - Jan 2019</a>
      </li>
      <li>
        <a href="https://flight-tracker.netlify.com/">Flight Tracker (Vue+OpenSky api) - Feb 2019</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
};
</script>
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
