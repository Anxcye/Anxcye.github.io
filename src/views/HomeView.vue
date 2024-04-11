<template>
  <div>
    <BlogHome />
    <div class="project-list">
      <ProjectItem
        v-for="project in projectList"
        :key="project.title"
        :project="project"
      />
    </div>
  </div>
</template>

<script>
import BlogHome from "../components/AboutMe.vue";
import ProjectItem from "../components/ProjectItem.vue";

export default {
  components: {
    BlogHome,
    ProjectItem,
  },
  setup() {
    return {
      projectList: [
        {
          title: "个人网页（本站）",
          description: "本站使用Vue3作为框架，部署于Github Pages",
          link: "anxcye.com",
          openSourceLink: "https://github.com/Anxcye/Anxcye.github.io",
        },
        {
          title: "ancy Blog",
          description:
            "一个功能丰富的个人博客。前端使用Vue3构建，后端使用Spring Boot构建",
          link: "https://blog.anxcye.com",
          openSourceLink: "https://github.com/Anxcye/ancy",
        },
        {
          title: "安读 Anx Reader",
          description: "支持多端同步的阅读器，使用flutter3构建，后端使用Spring Boot/Go构建",
          // link: "https://www.google.com",
          openSourceLink: "https://github.com/Anxcye/anx-reader",
        },
        {
          title: "m-shoping",
          description: "移动端购物页面，使用Vue2构建",
          link: "anxcye.com/m-shopping",
          openSourceLink: "https://github.com/Anxcye/m-shopping",
        },
      ],
    };
  },
};
</script>