<template>
  <div class="card">
    <img alt="screenshot" :src="'./img/' + link.img" class="screenshot" />
    <div class="details">
      <div class="header">{{ link.name }}</div>

      <p class="description">{{ link.summary }}</p>
      <div class="actions">
        <a :href="link.url" class="button" alt="demo" title="demo">DEMO</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['link'],
};
</script>
<style scoped>
img.screenshot {
  /* -webkit-filter: grayscale(100%); */
 filter: saturate(80%);
  opacity: 0.5;
  object-fit: cover;
  transition: 0.3s;
  height: 200px;
  border-top-left-radius: 4px;
  border-top-right-radius: 4px;
}

.card {
  display: flex;
  flex-direction: column;
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.5);
  transition: 0.3s;
  margin: 5px;
  border-radius: 4px;
  /* border: 1px solid #777; */
  /* border-top: 4px solid var(--colorl2); */
  background-color: var(--colord3);
}

.card:hover {
  filter: brightness(108%);
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.8);
}

.card:hover img.screenshot {
    /* -webkit-filter: grayscale(0); */
 filter: grayscale(0);
  opacity: 1;
}

.card .header {
  font-weight: bold;
  color: var(--colorf2);
}

.description {
  font-size: 0.9em;
  flex: 1;
  margin: 10px 0;
}

.actions {
  margin-top: 10px;
}

.details {
  display: flex;
  flex-direction: column;
  padding: 20px;
  flex: 1;
}

.button {
  text-decoration: none;
  /* font-weight: bold; */
  color: rgb(255, 152, 0);
  font-stretch: 100%;
}
</style>
