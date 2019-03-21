<template>
  <div id="app">
    <Cards v-bind:cards="categories" v-on:inc-like="incLike" />
    <!-- {{categories.id}} -->
  </div>
</template>

<script>
import Cards from './components/Cards.vue'

export default {
  name: 'app',
  components: {
    Cards
  },
  methods:{
    incLike(id){
            // this.categories.forEach(function(categories){
            //   if (categories.id == id){
            //   }
            // })
            this.categories[id-1]['rating'][0]['likes']++;
        }
  },
  data() {
    return {
      categories:[
        {
          id:1,
          picURL: 'https://previews.123rf.com/images/clumsyspace/clumsyspace1709/clumsyspace170900006/85777515-detailed-flat-blue-sedan-car-cartoon-with-shadow.jpg',
          about:[
            {
              class: 'Luxury',
              line: 'Go further'
            },
          ],
          rating:[
            {
              likes: 0,
              comments:['nice','good','could be better']
            }
          ]
        },
        {
          id:2,
          picURL: 'https://media-cdn.tripadvisor.com/media/photo-s/0c/98/a2/71/img-20160819-144334-largejpg.jpg', 

          about:[
            {
              class: 'Vintage',
              line: 'Count on us'
            },
          ],
          rating:[
            {
              likes: 6,
              comments:['awesome','good','could be better']
            }
          ]
        },
        {
          id:3,
          picURL: 'https://www.jeep-india.com/content/dam/cross-regional/apac/jeep/en_crossregional/history/1940s/vehicle-lineup/2018-Jeep-History-1940s-Vehicle-Lineup-Willys-MB.jpg.img.1440.jpg',
          about:[
            {
              class: 'Jeep',
              line: 'Something Special'
            },
          ],
          rating:[
            {
              likes: 5,
              comments:['nice','good','need improvements']
            }
          ]
        },
        {
          id:4,
          picURL: 'https://www.autocar.co.uk/sites/autocar.co.uk/files/styles/body-image/public/chevrolet-corvette-stingray.jpg?itok=p8IHD30y',
          about:[
            {
              class: 'Sports',
              line: 'Moving World'
            },
          ],
          rating:[
            {
              
              likes: 2,
              comments:['nice','amazing','could be better']
            }
          ]
        },
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
