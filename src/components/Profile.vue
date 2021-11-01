<template>
  <div class="main">
    <h3>andretan.nl</h3>
    <img alt="My avatar" class="avatar" src="../assets/avatar.svg">
    <div class="icons">
      <a
        v-for="link in links"
        :key="link.url"
        :href="link.url"
        :title="link.url"
        :class="`socicon socicon-${link.socicon}`"
      ></a>
    </div>
    <div class="links">
      <a href="https://lousycoder.netlify.com/">Blog</a>
    </div>
  </div>
</template>

<script>
const links = [
  {
    socicon: 'github',
    url: 'https://github.com/tanandre',
  },
  {
    socicon: 'firefox',
    url: 'https://gitlab.com/tanneman1',
  },
  {
    socicon: 'linkedin',
    url: 'https://www.linkedin.com/in/andre-tan-56a6445/',
  },
  {
    socicon: 'twitter',
    url: 'https://twitter.com/tan_andre',
  },
  {
    socicon: 'android',
    url: 'https://play.google.com/store/apps/developer?id=Andre+Tan',
  },
];

export default {
  data() {
    return {
      links,
    };
  },
};
</script>
<style scoped>
.main {
  margin: 30px 10px;
  text-align: center;
}

a.socicon {
  text-decoration: none;
  margin: 5px;
  vertical-align: middle;
  font-size: 1.5em;
}

.avatar {
  width: 200px;
  background-color:rgba(255,255,255,0.2);
  border-radius: 50%;
}

.icons {
  margin-top: 50px;
  margin-bottom: 20px;
}
</style>
