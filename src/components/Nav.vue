<template>
    <v-navigation-drawer
            v-model="drawer"
            :color="color"
            :expand-on-hover="expandOnHover"
            :permanent="permanent"
            :src="bg"
            absolute
            dark
    >
        <v-list
                dense
                nav
                class="py-0"
        >
            <v-list-item :class="'miniVariant && px-0'">
                <v-container>
                    <v-col :class="'py-0'">
                        <v-list-item-content :class="'py-0'">
                            <v-list-item-title>Jordan Hicks</v-list-item-title>
                        </v-list-item-content>
                    </v-col>
                    <v-col :class="'py-0'">
                        <v-list-item-content>
                            <v-list-item-subtitle :class="'text-center'">Full Stack Developer</v-list-item-subtitle>
                        </v-list-item-content>
                    </v-col>
                    <v-col :class="'text-center pa-0 m-0 ml-auto'">
                        <v-list-item-avatar rounded size="10rem">
                            <img src="../assets/jordan_profile.png">
                        </v-list-item-avatar>
                    </v-col>
                </v-container>
            </v-list-item>

            <v-divider></v-divider>

            <v-list-item
                    v-for="item in items"
                    :key="item.title"
                    link
            >
                <v-list-item-icon>
                    <v-icon>{{ item.icon }}</v-icon>
                </v-list-item-icon>

                <v-list-item-content>
                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                </v-list-item-content>
            </v-list-item>
        </v-list>
    </v-navigation-drawer>
</template>

<script>
  export default {
    data () {
      return {
        drawer: true,
        items: [
          { title: 'Portfolio', icon: 'mdi-view-dashboard' },
          { title: 'Experience', icon: 'mdi-image' },
          { title: 'Skills', icon: 'mdi-help-box' },
          { title: 'About', icon: 'mdi-help-box' },
        ],
        color: 'black',
        colors: [
          'primary',
          'blue',
          'success',
          'red',
          'teal',
          'black',
        ],
        right: false,
        permanent: true,
        miniVariant: false,
        expandOnHover: false,
        background: false,
      }
    },
    computed: {
      bg () {
        return this.background ? 'https://cdn.vuetifyjs.com/images/backgrounds/bg-2.jpg' : undefined
      },
    },
  }
</script>

<style scoped>

</style>