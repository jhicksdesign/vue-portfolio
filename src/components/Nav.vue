<template>
    <v-navigation-drawer
            app
            v-model="drawer"
            :color="color"
            :expand-on-hover="expandOnHover"
            :permanent="isLarge"
            :src="bg"
            dark
            fixed
    >
        <v-menu v-if="$vuetify.breakpoint.xsOnly"/>
        <v-list
                dense
                nav
                class="py-0"
        >
            <v-list-item :class="'miniVariant && px-0'">
                <v-container>
                    <v-col :class="'text-center pa-0 m-0 ml-auto'">
                        <v-list-item-avatar rounded size="10rem">
                            <img src="../assets/jordan_profile.png">
                        </v-list-item-avatar>
                    </v-col>
                    <v-col :class="'py-0'">
                        <v-list-item-content :class="'py-0'">
                            <v-list-item-title :class="'text-center'">Jordan Hicks</v-list-item-title>
                        </v-list-item-content>
                    </v-col>
                    <v-col :class="'py-0'">
                        <v-list-item-content>
                            <v-list-item-subtitle :class="'text-center'">Full Stack Developer</v-list-item-subtitle>
                        </v-list-item-content>
                    </v-col>
                </v-container>
            </v-list-item>

            <v-divider></v-divider>

            <v-list-item
                    v-for="item in items"
                    :key="item.title"
                    :to="item.link"
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
          { title: 'Portfolio', icon: 'mdi-view-dashboard', link: '/' },
          { title: 'Experience', icon: 'mdi-book', link: '/experience' },
          { title: 'Skills', icon: 'mdi-brain', link: '/skills' },
          { title: 'About', icon: 'mdi-help-box', link: '/about' },
          { title: 'Resume', icon: 'mdi-book', link: '/resume'}
        ],
        color: 'green',
        colors: [
          'primary',
          'blue',
          'success',
          'red',
          'teal',
          'black',
        ],
        right: false,
        permanent: false,
        miniVariant: false,
        expandOnHover: false,
        background: false,
      }
    },
    computed: {
      bg () {
        return this.background ? 'https://cdn.vuetifyjs.com/images/backgrounds/bg-2.jpg' : undefined
      },
      isLarge() {
        return this.$vuetify.breakpoint.name !== 'xs'
      }
    },
  }
</script>

<style scoped>
</style>