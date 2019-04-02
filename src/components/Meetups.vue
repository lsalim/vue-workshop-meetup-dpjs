<template>
   <main>
  <ul id="meetups">
    <li v-for="(meetup, index) in meetups" :key="index">
      <div class="event">
        <ul class="metadata">
          <li><h1>{{ meetup.name }}</h1></li>
          <li><span class="icon-date"></span> <span>{{ meetup.date }}</span></li>
          <li><span class="icon-location"></span> <span>{{ meetup.location }}</span></li>
        </ul>
        <div>
          <p class="meetup-avatar"><img v-bind:src="require(`@/assets/img/meetings/${meetup.avatar}`)"
            alt="dakar promise js"
            width="120"
            height="120"></p>
        </div>
      </div>
    </li>

    
  </ul>

</main>
</template>

<script>
export default {
    name: 'Meetups',
    data() {
        return {
            meetups: [
            { 
          "id": 1, 
          "name": "Dakar Promise JS", 
          "date": "2019-03-31",
          "location": "Edacy, Sacre Coeur",
          "avatar": "image-dpjs.png",
          "speakers": [
              { "name": "Thierno Thiam", "subject": "Building the same app in Angular", "title": "Software Engineer @ Sonatel", "avatar": "thiam.jpg" },  
              { "name": "Leyla Salim", "subject": "Building the same app in Vue.js", "title": "Software Engineer @ Makeba", "avatar": "salim.jpg" },  
              { "name": "Ibrahima Ciss", "subject": "Building the same app in React.js", "title": "Software Engineer @ Makeba", "avatar": "ciss.jpg" }  
          ] 
      },
      { 
          "id": 2, 
          "name": "GDG Dakar", 
          "date": "2019-01-19",
          "location": "Edacy, Sacre Coeur",
          "avatar": "image-gdg.png",
          "speakers": [
              { "name": "Mamadou Djigo", "subject": "Challenges of the startups in Senegal", "title": "Country Director @ Edacy", "avatar": "djigo.jpg" },  
              { "name": "Rygel Louv", "subject": "Kotlin Delegation", "title": "Software Engineer @ Makeba", "avatar": "louv.jpg" },  
              { "name": "Thierno Diop & Elias W Ba", "subject": "Machine Learning in the browser", "title": "-", "avatar": "two_speakers.jpg" },
              { "name": "Ibrahima Ciss", "subject": "VsCode Productivity guide", "title": "Software Engineer @ Makeba", "avatar": "ciss.jpg" }  
          ] 
      },
      { 
          "id": 3, 
          "name": "Galsen AI", 
          "date": "2019-01-12",
          "location": "ESP, Dakar",
          "avatar": "image-galsen-ai.png",
          "speakers": [
              { "name": "Ousmane Sarr", "subject": "IOT: applications, evolution of the offer, challenge and opportunities", "title": "Software Engineer @ Makeba", "avatar": "ousmane.jpg" },
              { "name": "Ahmadou H. Dicko, PhD", "subject": "Introduction to probabilistic statistical learning using gaussian process", "title": "Statistical Consultant", "avatar": "dicko.jpg" }  

          ] 
      },
      { 
          "id": 4, 
          "name": "Dakar Android U.G", 
          "date": "2018-11-24",
          "location": "Edacy, Sacre Coeur",
          "avatar": "image-daug.png",
          "speakers": [
              { "name": "Souleymane Sidine", "subject": "Android App Bundle", "title": "-", "avatar": "sidibe.jpg" },  
              { "name": "Martial Konvi", "subject": "Android CI with Jenkins", "title": "-", "avatar": "konvi.jpg" },  
              { "name": "Ibrahima Ciss", "subject": "MVC Done Right", "title": "Software Engineer @ Makeba", "avatar": "ciss.jpg" },
              { "name": "Kuassi Jimmy Kumako", "subject": "Google ML Kit", "title": "-", "avatar": "ciss.jpg" }  
          ] 
      }
    ]

        }
    },
}
</script>