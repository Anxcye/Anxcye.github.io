<template>
  <div>
    <div class="item">
      <h2 @click="openLink">{{ project.title }}</h2>
      <p>{{ project.description }}</p>
      <template v-if="project.link">
        <a :href="project.link" target="_blank">查看项目</a>
      </template>
      <template v-if="project.openSourceLink">
        <a :href="project.openSourceLink" target="_blank">源码地址</a>
      </template>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProjectItem",
  props: {
    // title: String,
    // description: String,
    // link: String,
    // openSourceLink: String,
    project: {
      type: Object,
      required: true,
    },
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