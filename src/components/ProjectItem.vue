<template>
  <div>
    <div class="item">
      <h2 @click="openLink">{{ title }}</h2>
      <p>{{ description }}</p>
      <template v-if="link">
        <a :href="link" target="_blank">查看项目</a>
      </template>
      <template v-if="openSourceLink">
        <a :href="openSourceLink" target="_blank">源码地址</a>
      </template>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProjectItem",
  props: {
    title: String,
    description: String,
    link: String,
    openSourceLink: String,
  },
  methods: {},
};
</script>

<style>
.item {
  padding: 1rem;
  border: 1px solid var(--color-border);
  border-radius: 0.5rem;
  margin-bottom: 1rem;
}
</style>