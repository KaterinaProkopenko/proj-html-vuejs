<template>
  <main>

    <section id="jumbotron" class="position-relative">
      <!-- Jumbo overlay -->
      <img id="jumbo-overlay" class="w-100 h-50 position-absolute bottom-0" src="../assets/img/jumbo-overlay.svg" alt="jumbo-overlay"/>

      <!-- Right menu -->
      <div class="menu position-absolute d-flex flex-column bg-light p-2 pt-0 gap-3 rounded">
        <a href="#">
          <img src="https://www.kindpng.com/picc/m/34-346527_ruler-triangle-drafting-triangle-icon-png-transparent-png.png" alt="ruler"/>
        </a>
        <a href="#" v-for="(element, index) in iconsListJumbo" :key="index">
          <i :class="element"></i>
        </a>
      </div>

      <div class="ms-container">
        <div class="row">
          <!-- Left content -->
          <div class="col-5 py-4 pe-5">
            <h1 class="main-color fw-bold mt-5 pt-3">
              Complete Your Dreams in JavaS Programming
            </h1>
            <p class="content-text py-2">
              Learn any coding program in distance and for a reasonable fee. You
              don't have to struggle alone, you've got our assistence and help.
            </p>
            <a @mouseover="btnDownloadFree = true" @mouseleave="btnDownloadFree = false" class="btn text-light py-2 px-4 fw-bold position-relative my-btn-fs" :class="btnDownloadFree ? 'hover-button' : 'static-button'">
              <i class="fas fa-download me-2" role="button"></i>
              Download free E-book
            </a>
          </div>

          <!-- Right image -->
          <div class="col-7 pt-4 text-end">
            <img
              class="main-img"
              src="../assets/img/home-5-hero-image.png"
              alt="Home hero image"
            />
          </div>
        </div>
      </div>
    </section>

    <section id="start-learning" class="mt-5">
      <div class="ms-container">

        <!-- Row of title -->
        <div class="row pt-3">
          <div class="col-12 text-center">

            <!-- Under title -->
            <h6 class="text-uppercase text-size pb-1">
              start learning coding languages
            </h6>

            <!-- Title -->
            <h1 class="d-inline-block fw-bold main-color">Build Your Dream</h1>
            <span class="text-uppercase fs-1 ps-2 in-title">today</span>
          </div>

          <!-- Cards-->
          <div class="col-12 d-flex gap-2">

            <!-- card -->
            <div class="card text-center border-0" v-for="(element, index) in startLearningCards" :key="index">
              <img :src="require(`../assets/img/${element.image}`)" class="card-img-top p-3" :alt="index"/>
              <h6 class="card-title py-2 text-dark fw-bold">{{ element.title }}</h6>
              <p class="text-size text-size main-color px-4">{{ element.text }}</p>
              <a href="#" class="my-btn text-size main-color fw-bold">Start now<i class="bi bi-arrow-right ps-2"></i></a>
            </div>
          </div>
        </div>

          
      </div>
    </section>

    <section id="career-perspective" class="position-relative mt-5">
      <img id="underlay-career" class="position-absolute" src="../assets/img/underlay-shape-lilla.svg" alt="underlay">

      <div class="ms-container">
        <div class="row pt-5">

          <!-- Left content -->
          <div class="col-6">
            <img class="position-relative ms-5" src="../assets/img/about-us-03-image-01.png" alt="About us">
          </div>

          <!-- Right content -->
          <div class="col-6">

            <!-- Under title -->
            <h6 class="text-uppercase text-size m-0">
              dream with <span class="fw-bold">maxcoach</span>
            </h6>

            <!-- Title -->
            <h1 class="d-inline-block fw-bold main-color m-0 py-3">Construct A <span class="fs-1 ps-2 in-title fw-normal">Stunning</span> Career Perspective</h1>
            
            <!-- Content -->
            <div class="content w-100 mt-3">

              <!-- Buttons -->
              <div class="button-content w-100">

                <!-- Button active -->
                <a class="btn text-light py-2 px-4 fw-bold btn-active my-btn-fs w-100">
                  Multiple Platforms Supported for Teaching & Studing
                  <i class="fas fa-minus-circle ps-5"></i>
                </a> 
                <p class="text-size main-color bg-light p-3 w-100 rounded-bottom m-0 shadow">MaxCoach supports the act of teaching and learning on multiple platforms like online or offline via material downloads. We know things aren't supposed to be devoured in a short time, you can always access our knowledge base from any device.</p>

                <a class="btn bg-light py-2 px-4 fw-bold my-btn-fs my-4 w-100 shadow">
                  Multiple Platforms Supported for Teaching & Studing
                  <i class="fas fa-plus-circle ps-5"></i>
                </a>

                <a class="btn bg-light py-2 px-4 fw-bold my-btn-fs w-100 shadow">
                  Multiple Platforms Supported for Teaching & Studing
                  <i class="fas fa-plus-circle ps-5"></i>
                </a>

              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="statistics">
      <div class="ms-container h-100">
        <div class="row w-100 h-100">
          <div class="col-12 w-100 h-100 d-flex align-items-center">

            <!-- card -->
            <div v-for="(element, index) in statistics" :key="index" class="statistics-element text-center">
              <h1 class="fw-bold">{{element.number}}</h1>
              <h6 class="text-uppercase text-size m-0 fw-bold">{{element.text}}</h6>
            </div>

          </div>
        </div>
      </div>
    </section>

    <section id="courses" class="position-relative">
      <!-- Background -->
      <div class="bg-color w-100 h-100 position-absolute top-0"></div>

      <div class="ms-container position-relative">

        <div class="row pt-3">
          <!-- Container of title -->
          <div class="col-12 text-center">

            <!-- Under title -->
            <h6 class="text-uppercase text-size pb-1">
              choose where you'd like to begin
            </h6>

            <!-- Title -->
            <h1 class="d-inline-block fw-bold main-color">Latest Featured</h1>
            <span class="fs-1 ps-2 in-title">Courses</span>
          </div>

          <!-- Container of cards -->
          <div class="col-12 d-flex gap-2 w-100 flex-wrap justify-content-center gap-3">

            <!-- card -->
            <div @mouseover="getHoverCard(index)" @mouseleave="leaveHoverCard(index)"  v-for="(element, index) in coursesCards" :key="index" :class="(element.hoverEffect) ? 'shadow bg-light' : 'bg-transparent'" class="card border-0 w-25 position-relative">
              <img class="rounded-top" :src="require(`../assets/img/${element.image}`)" alt="Card-image">
              <div class="price position-absolute top-0 end-0 my-btn-fs py-1 px-3 fw-bold text-light"><span class="fs-6">{{element.priceHead}}</span>{{element.priceBody}}</div>
              <div class="card-body">

                <div class="teacher mb-3">
                  <img class="rounded-circle" :src="require(`../assets/img/${element.imageTeacher}`)" :alt="element.nameTeacher">
                  <p class="text-size main-color m-0 d-inline-block ps-3">{{element.nameTeacher}}</p>
                </div>

                <h6 class="card-title text-dark fw-bold mb-4">{{element.title}}</h6>

                <div class="short-description d-flex text-size main-color">
                  <div class="lessons">
                    <i class="bi bi-journal-text px-1"></i>
                    <p class="d-inline-block px-2 mb-0">{{element.lessons}} Lessons</p>
                  </div>

                  <div class="students ps-4">
                    <i class="far fa-user px-1"></i>
                    <p class="d-inline-block px-2 mb-0">{{element.students}} Students</p>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Container of button -->
          <div class="col-12 text-center pt-4">
            <a @mouseover="viewAllCourses = true" @mouseleave="viewAllCourses = false" class="btn text-light py-2 px-4 fw-bold position-relative my-btn-fs" :class="viewAllCourses ? 'hover-button' : 'static-button'">
              View all courses
              <i class="bi bi-arrow-right p1-2" role="button"></i>
            </a>
          </div>
      </div>
    </section>

    <section id="your-pace" class="position-relative mt-5">
      <img id="underlay-your-pace" class="position-absolute" src="../assets/img/underlay-shape-grey.svg" alt="underlay">
      <img id="underlay-your-pace-shape" class="position-absolute rounded-circle" src="../assets/img/maxcoach-shape-07-150x150.png" alt="underlay"> 


      <div class="ms-container">
        <div class="row pt-5">

          <!-- Left content -->
          <div class="col-6 position-relative px-5">

            <!-- Under title -->
            <h6 class="text-uppercase text-size m-0">why hesitate to register?</h6>

            <!-- Title -->
            <h1 class="d-inline-block fw-bold main-color m-0 pt-3">Learn At Your Own <span class="fs-1 ps-2 in-title fw-normal">Pace</span></h1>
            
            <!-- Content -->
            <div class="content w-100 mt-3">

              <!-- Unordered list -->
              <ul class="ps-0 mb-4">
                <li v-for="(element, index) in yourPaceList" :key="index" class="lh-lg">
                  <i class="fas fa-check fs-6"></i>
                  <h6 class="main-color d-inline-block ps-4">{{element.listElement}}</h6>
                </li>
              </ul>

              <!-- Button -->
              <a @mouseover="btnGetStartedFree = true" @mouseleave="btnGetStartedFree = false" class="btn text-light py-2 px-4 fw-bold position-relative my-btn-fs" :class="btnGetStartedFree ? 'hover-button' : 'static-button'">
                Get started for free
              </a>
              
            </div>
          </div>

          <!-- right content -->
          <div class="col-6">
            <img id="your-pace-main-img" class="position-relative" src="../assets/img/home-5-image-01.png" alt="Learn at your own pace">
          </div>

          
        </div>
      </div>
    </section>

    <section id="learn-in-mobile" class="position-relative mt-5">
      <img id="underlay-mobile" class="position-absolute" src="../assets/img/underlay-shape-grey.svg" alt="underlay">
      <img id="underlay-mobile-shape-lines" src="../assets/img/maxcoach-shape-01.png" class="position-absolute" alt="Maxcoach shape">
      <img id="underlay-mobile-shape-squares" src="../assets/img/maxcoach-shape-07.png" class="position-absolute" alt="Maxcoach shape">

      <div class="ms-container">
        <div class="row pt-5">

          <!-- Left content -->
          <div class="col-6 text-center">
            <img id="learn-mobile-main-img" class="position-relative" src="../assets/img/home-5-image-02.png" alt="Learn in mobile">
          </div>
          
          <!-- Right content -->
          <div class="col-6 position-relative p-5">

            <!-- Under title -->
            <h6 class="text-uppercase text-size m-0">what are you looking for?</h6>

            <!-- Title -->
            <h1 class="d-inline-block fw-bold main-color m-0 pt-3">Learn on your <span class="fs-1 ps-2 in-title fw-normal">mobile</span> anytime!</h1>
            
            <!-- Content -->
            <div class="content w-100 mt-3">

              <p class="text-size main-color ">Save lessons for later and revise or write notes at any time and on multiple devices on your way. Never interfere with activites of enjoyment or other precious moments.</p>

              <!-- Button -->
              <a @mouseover="btnDownloadApp = true" @mouseleave="btnDownloadApp = false" class="btn text-light py-2 px-4 fw-bold position-relative my-btn-fs" :class="btnDownloadApp ? 'hover-button' : 'static-button'">
                Download Our App
              </a>
              
            </div>
          </div>

          
        </div>
      </div>
    </section>
  </main>

  
  
</template>

<script>
export default {
  name: "mainIndex",
  data: function () {
    return {
      iconsListJumbo: ["far fa-dot-circle", "fas fa-book", "bi bi-cart3"],
      btnDownloadFree: false,
      viewAllCourses: false,
      btnGetStartedFree: false,
      btnDownloadApp: false,
      startLearningCards: [
        {
          image: "home-5-image-box-01.png",
          title: "Idea Discussion",
          text: "Get teamed up with the specialists who work and teach coding fpr years at famous universities.",
          upStartNow: false,
        },
        {
          image: "home-5-image-box-02.png",
          title: "Web Development",
          text: "Learn to start building a webpage from scratch. You decide your own pace, course and speed.",
          upStartNow: false,
        },
        {
          image: "home-5-image-box-03.png",
          title: "System Administration",
          text: "Learners are encouraged to study the mechanism and structure of system administration.",
          upStartNow: false,
        },
        {
          image: "home-5-image-box-04.png",
          title: "Graphic Design",
          text: "Have a passion for graphics and arts? Show your talents with confidence and self-assertiveness.",
          upStartNow: false,
        },
      ],
      statistics: [
        {
          number: 1.926,
          text: 'finished sessions'
        },
        {
          number: '3.092+',
          text: 'enrolled learners'
        },
        {
          number: 200,
          text: 'online instructors'
        },
        {
          number: '100%',
          text: 'satisfaction rate'
        }
      ],
      coursesCards: [
        {
          priceHead: '$40',
          priceBody: '.00',
          image: 'course-02-480x298.jpg',
          imageTeacher: '73ee246daf47502812ccefc84bf02898.jpeg',
          nameTeacher: 'Blanche Fields',
          title: 'Learning to Write as a Professional Author',
          lessons: 20,
          students: 50,
          hoverEffect: false
        },
        {
          priceBody: 'Free',
          image: 'stock-full-hd-03-480x298.jpg',
          imageTeacher: 'd0d504142acfde820eef2f11feea6253.jpeg',
          nameTeacher: 'Maggie Strickland',
          title: 'Customer-centric Info-Tech Strategies',
          lessons: 24,
          students: 769,
          hoverEffect: false
        },
        {
          priceHead: '$19',
          priceBody: '.00',
          image: 'stock-full-hd-04-480x298.jpg',
          imageTeacher: 'd0d504142acfde820eef2f11feea6253.jpeg',
          nameTeacher: 'Maggie Strickland',
          title: 'Open Programming Courses for Everyone: Python',
          lessons: 17,
          students: 62,
          hoverEffect: false
        },
        {
          priceHead: '$26',
          priceBody: '.00',
          image: 'stock-full-hd-06-480x298.jpg',
          imageTeacher: '73ee246daf47502812ccefc84bf02898.jpeg',
          nameTeacher: 'Blanche Fields',
          title: 'Academic Listening and Note-taking',
          lessons: 14,
          students: 67,
          hoverEffect: false
        },
        {
          priceHead: '$39',
          priceBody: '.00',
          image: 'course-featured-image-01-480x298.jpg',
          imageTeacher: '73ee246daf47502812ccefc84bf02898.jpeg',
          nameTeacher: 'Blanche Fields',
          title: 'Master jQuery in a Short Period of Time',
          lessons: 6,
          students: 51,
          hoverEffect: false
        },
        {
          priceHead: '$59',
          priceBody: '.00',
          image: 'stock-full-hd-05-480x298.jpg',
          imageTeacher: '73ee246daf47502812ccefc84bf02898.jpeg',
          nameTeacher: 'Blanche Fields',
          title: 'Introduction to Javascript for Beginners',
          lessons: 14,
          students: 76,
          hoverEffect: false
        },
      ],
      yourPaceList: [
        {
          listElement: 'Select & customize courses to your preferences'
        },
        {
          listElement: 'Change the tutor and make arrangements'
        },
        {
          listElement: 'Participate in events to join others'
        },
        {
          listElement: 'Get the desired certificate delivered at house'
        }
      ],
    };
  },
  methods: {

    getHoverCard(index){
      this.coursesCards[index].hoverEffect = true;
    },

    leaveHoverCard(index){
      this.coursesCards[index].hoverEffect = false;
    }
  }
};
</script>

<style lang="scss" scoped>
@import "../assets/style/_variables.scss";

main {
  width: 100%;

  section#jumbotron {
    width: 100%;
    height: 600px;
    background-color: $brandPrimary;

    img#jumbo-overlay {
      transform: rotate(180deg);
      transform: scaleY(-1);
    }

    div.menu {
      right: 0;
      top: 90px;

      a {
        color: black;

        img {
          width: 16px;
        }

        i {
          font-size: 1rem;
        }
      }
    }

    div.ms-container {
      img.main-img {
        width: 500px;
      }

      p.content-text {
        color: $brandColorContentText;
      }
    }
  }

  section#start-learning {
    div.card {
      width: calc(100% / 4);
      

      img {
        width: 140px;
        height: 160px;
        margin: 0 auto;
      }

      a.my-btn{
/*         color: $brandColorContentText; */
        transition: .4s;
      }

      a.my-btn:hover{
        color: $brandColorTextSecondary;
      }
    }
  }

  section#career-perspective{
    img#underlay-career{
      width: 295px;
      bottom: 45px;
      left: 150px;
    }

    div.ms-container{
      img{
        height: 400px;
      }

      div.button-content{
        opacity: .8;

        a.btn-active{
          background-color: $brandColorTextSecondary;
          border-radius: .25rem .25rem 0 0;
        }

        a{
          color: $brandColorTextPrimary;
        }
      }
    }

    
  }

  section#statistics{
    background-color: $brandPrimary;
    height: 160px;
    margin-top: 70px;

    div.statistics-element{
      width: calc(100% / 4);

      h1{
        color: $brandColorTextSecondary;
      }

      h6{
          color: $brandColorTextPrimary;
        }
      }
  }

  section#courses{
    width: 100%;
    height: 900px;
    margin-top: 70px;

    div.bg-color{
      background: $brandPrimary;
      background: linear-gradient(0deg, rgba(240,239,239,1) 0%, rgba(255,255,255,1) 100%);
      border-radius: 0 0 38% 38%;
    }

    div.ms-container{
      div.card{
        width: calc(100% / 3);

        div.price{
        background-color: $brandColorTextSecondary;
        border-radius: 0 .25rem 0 .25rem;
       }
      }
      
    }
  }

  section#your-pace{
    height: 500px;

    img#underlay-your-pace{
      width: 330px;
      right: 32%;
      bottom: 30px;
    }

    img#underlay-your-pace-shape{
      right: 20%;
      bottom: 100px;
    }

    img#your-pace-main-img{
      width: 60%;
    }
    i{
      color: $brandColorTextSecondary;
    }
  }

  section#learn-in-mobile{
    height: 440px;

    img#underlay-mobile{
      width: 330px;
      bottom: 0;
      left: 240px;
    }

    img#underlay-mobile-shape-squares{
      width: 70px;
      height: 110px;
      bottom: 70px;
      left: 40%;
    }

    img#underlay-mobile-shape-lines{
      width: 90px;
      top: 210px;
      left: 180px;

    }

    img#learn-mobile-main-img{
      width: 50%;
    }
  }
}
</style>