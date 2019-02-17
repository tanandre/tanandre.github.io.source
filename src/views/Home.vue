<template>
  <div class="wrapper">
    <!-- <header class="main-head">The header</header> -->
    <nav class="main-nav">
      <Profile/>
    </nav>
    <article class="content">
      <ProjectLinks msg="Welcome to Your Vue.js App"/>
    </article>
  </div>
</template>

<script>
import ProjectLinks from '@/components/ProjectLinks.vue';
import Profile from '@/components/Profile.vue';

export default {
  name: 'home',
  components: {
    ProjectLinks,
    Profile,
  },
};
</script>
<style scoped>
.main-head {
  grid-area: header;
}
.content {
  grid-area: content;
  padding: 10px 20px;
}
.main-nav {
  grid-area: nav;
  background-color: rgb(68, 75, 84);
  height: 100vh;
}
.side {
  grid-area: sidebar;
}
.ad {
  grid-area: ad;
}
.main-footer {
  grid-area: footer;
}
.wrapper {
  display: grid;
  grid-gap: 0px;
  grid-template-areas:
    "header"
    "nav"
    "content"
    "sidebar"
    "ad"
    "footer";
}

@media (min-width: 500px) {
  .wrapper {
    grid-template-columns: 1fr 3fr;
    grid-template-areas:
      "header  header"
      "nav     nav"
      "sidebar content"
      "ad      footer";
  }
  nav ul {
    display: flex;
    justify-content: space-between;
  }
}

@media (min-width: 700px) {
  .wrapper {
    grid-template-columns: 1fr 4fr 1fr;
    grid-template-areas:
      "header header  header"
      "nav    content sidebar"
      "nav    content ad"
      "footer footer  footer";
  }
  nav ul {
    flex-direction: column;
  }
}
</style>
