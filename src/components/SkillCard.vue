<template>
    <v-container>
        <h1>Proficient Technical Skills</h1>
        <v-row class="justify-center">
            <v-sheet
                    height="100"
                    width="100"
                    :key="i" v-for="(skills, i) in skills" class="ma-5 d-block"
            >
                <div class="my-auto">
                    <v-icon x-large>{{skills.icon}}</v-icon>
                    <h3>{{skills.title}}</h3>
                </div>
            </v-sheet>
        </v-row>
    </v-container>
</template>

<script>
  export default {
    name: "SkillCard",
    props: ["skills"]
  }
</script>

<style scoped>

</style>