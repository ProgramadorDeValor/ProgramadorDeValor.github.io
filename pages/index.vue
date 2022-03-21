<template>
  <v-container>
    <v-row class="justify-center">
      <v-col cols="12">
        <about id="about" />
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        <project id="project" />
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        <skills id="skills" />
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        <resume id="resume" />
      </v-col>
    </v-row>
  </v-container>
</template>
<style scoped>

</style>
<script>
import About from '@/pages/about'
import Project from '@/pages/project'
import Resume from '@/pages/resume'
import Skills from '@/pages/skills'

export default {
  name: 'Index',
  components: {
    About,
    Project,
    Resume,
    Skills
  }
}
</script>
