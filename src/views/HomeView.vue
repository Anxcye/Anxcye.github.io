<template>
  <div>
    <BlogHome />
    <div class="project-list">
      <ProjectItem
        v-for="project in projectList"
        :key="project.title"
        :title="project.title"
        :description="project.description"
        :link="project.link"
        :openSourceLink="project.openSourceLink"
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
          title: "个人网站（本站）",
          description: "本站使用Vue3作为框架，部署于Github Pages",
          link: "anxcye.com",
          openSourceLink: "https://github.com/Anxcye/Anxcye.github.io"
        },
        {
          title: "Project 2",
          description: "This is a description of project 2",
          link: "https://www.google.com",
        },
        {
          title: "Project 3",
          description: "This is a description of project 3",
          link: "https://www.google.com",
        },
        {
          title: "Project 4",
          description: "This is a description of project 4",
          link: "https://www.google.com",
        },
        {
          title: "Project 5",
          description: "This is a description of project 5",
          link: "https://www.google.com",
        },
        {
          title: "Project 6",
          description: "This is a description of project 6",
          link: "https://www.google.com",
        },
        {
          title: "Project 7",
          description: "This is a description of project 7",
          link: "https://www.google.com",
        },
        {
          title: "Project 8",
          description: "This is a description of project 8",
          link: "https://www.google.com",
        },
        {
          title: "Project 9",
          description: "This is a description of project 9",
          link: "https://www.google.com",
        },
        {
          title: "Project 10",
          description: "This is a description of project 10",
          link: "https://www.google.com",
        },
      ],
    };
  },
};
</script>