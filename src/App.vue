<template>
    <div class="main">
        <div class="main-first">
             <div :class="imageClass" >     </div>              
              <div class="iconsone">  
                        <i  :id="Hearted" class="fa fa-heart heart icon1" @click="heartedFunc" aria-hidden="true"></i>
                        <a href="https://www.youtube.com/watch?v=HhoATZ1Imtw&ab_channel=SiaVEVO" target="blank">  
                        <i class="fa fa-external-link-square icon1"  aria-hidden="true"></i>   </a>
                        <i class="fa fa-arrow-right icon1"   aria-hidden="true" @click="changeImageClass"></i>
                        <i class="fa fa-arrow-left icon1" @click="decrementClass" aria-hidden="true"></i>   
             </div>
            <div class="audio" > 
                        <audio  class="audio-1" v-if="classNumber==1"  controls autoplay >
                        <source  class="source1"  :src="tracks[1].source">
                        </audio>
                
                        <audio  class="audio-1" v-if="classNumber==2" controls autoplay >
                        <source  class="source1"  :src="tracks[2].source">
                        </audio>             

                           <audio  class="audio-1" v-if="classNumber==3" controls autoplay >
                        <source  class="source1"  :src="tracks[3].source">
                        </audio>      

                           <audio  class="audio-1" v-if="classNumber==4" controls autoplay >
                        <source  class="source1"  :src="tracks[4].source">
                        </audio>      

                           <audio  class="audio-1" v-if="classNumber==5" controls autoplay >
                        <source  class="source1"  :src="tracks[5].source">
                        </audio>      

                           <audio  class="audio-1" v-if="classNumber==6" controls autoplay >
                        <source  class="source1"  :src="tracks[6].source">
                        </audio>      
            </div>
        </div>
    </div>

</template>

<script>


export default {
  name: 'Slider',
  components: {
    
  },
  data() {
      return {
         
          imageClass: "main-image",
          isHearted: false,
          Hearted: "",
          classNumber: 1,
          musicNumber: 5,
           tracks: [
        {
          name: "Mekanın Sahibi",
          artist: "Norm Ender",
          cover: "https://raw.githubusercontent.com/muhammederdem/mini-player/master/img/1.jpg",
          source: "https://raw.githubusercontent.com/muhammederdem/mini-player/master/mp3/1.mp3",
          url: "https://www.youtube.com/watch?v=z3wAjJXbYzA",
          favorited: false
        },
        {
          name: "Everybody Knows",
          artist: "Leonard Cohen",
          cover: "https://raw.githubusercontent.com/muhammederdem/mini-player/master/img/2.jpg",
          source: "https://raw.githubusercontent.com/muhammederdem/mini-player/master/mp3/2.mp3",
          url: "https://www.youtube.com/watch?v=Lin-a2lTelg",
          favorited: true
        },
        {
          name: "Extreme Ways",
          artist: "Moby",
          cover: "https://raw.githubusercontent.com/muhammederdem/mini-player/master/img/3.jpg",
          source: "https://raw.githubusercontent.com/muhammederdem/mini-player/master/mp3/3.mp3",
          url: "https://www.youtube.com/watch?v=ICjyAe9S54c",
          favorited: false
        },
        {
          name: "Butterflies",
          artist: "Sia",
          cover: "https://raw.githubusercontent.com/muhammederdem/mini-player/master/img/4.jpg",
          source: "https://raw.githubusercontent.com/muhammederdem/mini-player/master/mp3/4.mp3",
          url: "https://www.youtube.com/watch?v=kYgGwWYOd9Y",
          favorited: false
        },
        {
          name: "The Final Victory",
          artist: "Haggard",
          cover: "https://raw.githubusercontent.com/muhammederdem/mini-player/master/img/5.jpg",
          source: "https://raw.githubusercontent.com/muhammederdem/mini-player/master/mp3/5.mp3",
          url: "https://www.youtube.com/watch?v=0WlpALnQdN8",
          favorited: true
        },
        {
          name: "Genius ft. Sia, Diplo, Labrinth",
          artist: "LSD",
          cover: "https://raw.githubusercontent.com/muhammederdem/mini-player/master/img/6.jpg",
          source: "https://raw.githubusercontent.com/muhammederdem/mini-player/master/mp3/6.mp3",
          url: "https://www.youtube.com/watch?v=HhoATZ1Imtw",
          favorited: false
        },
        {
          name: "The Comeback Kid",
          artist: "Lindi Ortega",
          cover: "https://raw.githubusercontent.com/muhammederdem/mini-player/master/img/7.jpg",
          source: "https://raw.githubusercontent.com/muhammederdem/mini-player/master/mp3/7.mp3",
          url: "https://www.youtube.com/watch?v=me6aoX0wCV8",
          favorited: true
        },
        {
          name: "Overdose",
          artist: "Grandson",
          cover: "https://raw.githubusercontent.com/muhammederdem/mini-player/master/img/8.jpg",
          source: "https://raw.githubusercontent.com/muhammederdem/mini-player/master/mp3/8.mp3",
          url: "https://www.youtube.com/watch?v=00-Rl3Jlx-o",
          favorited: false
        },
        {
          name: "Rag'n'Bone Man",
          artist: "Human",
          cover: "https://raw.githubusercontent.com/muhammederdem/mini-player/master/img/9.jpg",
          source: "https://raw.githubusercontent.com/muhammederdem/mini-player/master/mp3/9.mp3",
          url: "https://www.youtube.com/watch?v=L3wKzyIN1yk",
          favorited: false
        }
      ],
      }
  },
  methods: {
    heartedFunc() {
          this.isHearted = true;
        if(this.isHearted == true) {
             this.Hearted = "love";
        }

    },
      
    changeImageClass() {
       
        this.classNumber ++;
        if (this.classNumber == 7) {
            this.classNumber = 1
        }
        if (this.classNumber ==1) {
            this.imageClass = "main-image "
        }
        if (this.classNumber==2) {
         this.imageClass = "main-image2 "
        }
  
         if (this.classNumber==3) {
         return   this.imageClass = "main-image3    "
        }
         if (this.classNumber==4) {
        return   this.imageClass = "main-image4  "
        }
         if (this.classNumber==5) {
          return  this.imageClass = "main-image5  "
        }
         if (this.classNumber==6) {
        return    this.imageClass = "main-image6  "
        }
        
    }  ,
    decrementClass() {
        
        this.classNumber --
        if (this.classNumber==0) {
            this.classNumber = 6
        }
        if (this.classNumber==1) {
         this.imageClass = "main-image  "
        }
            if (this.classNumber==2) {
         this.imageClass = "main-image2 "
        }
        console.log(this.imageClass)
         if (this.classNumber==3) {
         return   this.imageClass = "main-image3"
        }
         if (this.classNumber==4) {
         return   this.imageClass = "main-image4"
        }
         if (this.classNumber==5) {
          return  this.imageClass = "main-image5 "
        }
         if (this.classNumber==6) {
        return    this.imageClass = "main-image6"
        }
    } 
  }
  
}
</script>

<style lang="scss">
     @import "./scss/reset.scss";
     @import "./scss/main.scss";



</style>
