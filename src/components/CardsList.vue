<template>
  <transition name="fade" appear>
    <v-layout wrap>
      <v-flex xs12 class="align-stretch">
        <v-card-title class="headline mt-4 teal--text text--darken-2">
          A few side projects</v-card-title
        >
      </v-flex>
      <v-flex
        xs12
        sm6
        v-for="project in projects"
        :key="project.id"
        class="d-flex align-stretch pa-5 pa-sm-10 pt-sm-5"
      >
        <v-card class="pa-4">
          <v-img
            class="white--text align-end"
            height="370"
            :src="project.imagepath"
          >
          </v-img>
          <v-card-title class="headline mb-4 mt-4 teal--text text--darken-2">{{
            project.title
          }}</v-card-title>

          <v-card-subtitle class="subtitle-1 black--text">{{
            project.description
          }}</v-card-subtitle>

          <v-card-text class="text--primary">
            <code
              class="mr-4 mb-4 pa-1 subtitle-2"
              v-for="language in project.listOflanguages"
              :key="language"
            >
              {{ language }}
            </code>
          </v-card-text>
          <v-divider></v-divider>

          <v-btn
            medium
            class="ma-2 mb-0 white--text"
            color="teal accent-4"
            :href="project.viewProjectUrl"
          >
            view project
          </v-btn>

          <v-btn
            medium
            class="ma-2 mb-0 white--text"
            color="teal accent-4"
            :href="project.checkRepositoryUrl"
            >check git repo
          </v-btn>
        </v-card>
      </v-flex>

      <v-flex
        xs12
        sm6
        class="d-flex align-stretch pa-5 pa-sm-10 pt-sm-5"
        :key="6"
      >
        <v-card class="pa-4">
          <iframe
            width="100%"
            height="550"
            src="https://gretak.github.io/react-slider/"
          ></iframe>

          <v-card-title class="headline mb-4 mt-4 teal--text text--darken-2">
            "One day" slider
          </v-card-title>

          <v-card-subtitle class="subtitle-1 black--text">
            Resposive paralax slider made with React JS. The idea was to use it
            for presentations.
          </v-card-subtitle>

          <v-card-text class="text--primary">
            <code class="mr-4 mb-4 pa-1 subtitle-2">REACT</code>
            <code class="mr-4 mb-4 pa-1 subtitle-2">REACT spring</code>
            <code class="mr-4 mb-4 pa-1 subtitle-2">WEBPACK</code>
            <code class="mr-4 mb-4 pa-1 subtitle-2">HTML</code>
            <code class="mr-4 mb-4 pa-1 subtitle-2">SASS</code>
          </v-card-text>
          <v-divider></v-divider>

          <v-btn
            medium
            class="ma-2 mb-0 white--text"
            color="teal accent-4"
            href="https://gretak.github.io/react-slider/"
          >
            view project
          </v-btn>

          <v-btn
            medium
            class="ma-2 mb-0 white--text"
            color="teal accent-4"
            href="https://github.com/gretak/react-slider"
            >check git repo
          </v-btn>
        </v-card>
      </v-flex>
    </v-layout>
  </transition>
</template>

<script>
export default {
  name: 'CardsList',

  data() {
    return {
      projects: [
        {
          id: 1,
          title: 'Images API with VUE',
          description:
            'Listing 5000 images using VUE.JS and API.Using pagination, sorting, displaying last clicked data and other features. Project is hosted on github.',
          listOflanguages: [
            'HTML',
            'CSS',
            'JS',
            'VUEX',
            'AXIOS API',
            'VUE ROUTER',
            'BOOTSTRAPVUE'
          ],
          viewProjectUrl: 'https://gretak.github.io/list-of-images/',
          checkRepositoryUrl: 'https://github.com/gretak/list-of-images',
          imagepath: require('../assets/project-list-of-images.png')
        },
        {
          id: 2,
          title: 'Restaurants list with VUE',
          description:
            "Listing restaurants using VUE JS and API. Clicking on the restaurant 'contact us' button it reveals more details, which are pulled from API.",
          listOflanguages: [
            'HTML',
            'CSS',
            'JS',
            'VUEX',
            'AXIOS API',
            'VUE ROUTER',
            'VUE CLI'
          ],
          viewProjectUrl: 'https://gretak.github.io/restaurants-list/',
          checkRepositoryUrl: 'https://github.com/gretak/restaurants-list/',
          imagepath: require('../assets/project-list-of-restaurants.png')
        },
        {
          id: 3,
          title: 'Mobile App templates',
          description:
            "Fully responsive html mobile templates' button it reveals more details, which are pulled from API.",
          listOflanguages: ['HTML', 'CSS', 'JS', 'SLICK JS', 'FITTEXT JS'],
          viewProjectUrl:
            'https://gretak.herokuapp.com/mobile-templates/data/public/app/core/templates/alltogether.html',
          checkRepositoryUrl: 'https://github.com/gretak/Mobile-App-templates',
          imagepath: require('../assets/project-alltemplates.png')
        },
        {
          id: 4,
          title: 'React puzzle',
          description:
            'Responsive Puzzle Game. Has 3 levels, need to make an image by clicking on the squares.',
          listOflanguages: ['HTML', 'CSS', 'JS', 'REACT', 'WEBPACK', 'SASS'],
          viewProjectUrl: 'https://gretak.herokuapp.com/puzzle/',
          checkRepositoryUrl: 'https://github.com/gretak/react-slider',
          imagepath: require('../assets/project-puzzle.png')
        },
        {
          id: 5,
          title: 'Portfolio website',
          description:
            'I wanted to create a new website for my side projects. This was a great chance to try vue animations and Vuetify.',
          listOflanguages: [
            'VUE',
            'ANIMATING VUE',
            'VUE ROUTER',
            'AXIOS DOWNLOAD',
            'VUETIFY',
            'MATERIAL DESIGN/ICONS',
            'HTML',
            'CSS',
            'JS'
          ],
          viewProjectUrl: '/',
          checkRepositoryUrl: 'https://github.com/gretak/portfolio',
          imagepath: require('../assets/portfolio.png')
        },
        {
          id: 6,
          title: 'Project in progress',
          description:
            'I wanted to use vue forms and authentication. This project is in progress, will upload the MVP once available.',
          listOflanguages: [
            'VUE',
            'VUE FORMS',
            'BASIC AUTH',
            'VUE ROUTER',
            'AXIOS',
            'VUETIFY',
            'MATERIAL DESIGN/ICONS',
            'HTML',
            'CSS',
            'JS'
          ],
          viewProjectUrl: '/',
          checkRepositoryUrl: 'https://github.com/gretak/portfolio',
          imagepath: require('../assets/contact-form.png')
        }
      ]
    };
  }
};
</script>
