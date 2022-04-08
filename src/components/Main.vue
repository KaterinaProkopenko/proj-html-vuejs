<template>
  <main>

    <section id="jumbotron" class="position-relative">
        <!-- Jumbo overlay -->
        <img id="jumbo-overlay" class="w-100 h-50 position-absolute bottom-0" src="../assets/img/jumbo-overlay.svg" alt="jumbo-overlay">

        <!-- Right menu -->
        <div class="menu position-absolute d-flex flex-column bg-light p-2 pt-0 gap-3 rounded">
            <a href="#">
                <img id src="https://www.kindpng.com/picc/m/34-346527_ruler-triangle-drafting-triangle-icon-png-transparent-png.png" alt="ruler">
            </a>
            <a href="#" v-for="(element, index) in iconsListJumbo" :key="index">
                <i :class="element"></i>
            </a>
        </div>

        <div class="ms-container">
            <div class="row">

                <!-- Left content -->
                <div class="col-5 py-4 pe-5">
                    <h1 class="title fw-bold mt-5 pt-3">Complete Your Dreams in JavaS Programming</h1>
                    <p class="content-text py-2">Learn any coding program in distance and for a reasonable fee. You don't have to struggle alone, you've got our assistence and help.</p>
                    <a @mouseover="upHere = true" @mouseleave="upHere = false" class="btn text-light py-2 px-4 fw-bold position-relative" :class="(upHere) ? 'hover-button' : 'static-button'"><i class="fas fa-download me-2" role="button"></i>Download free E-book</a>
                </div>

                <!-- Right image -->
                <div class="col-7 pt-4 text-end">
                    <img class="main-img" src="../assets/img/home-5-hero-image.png" alt="Home hero image">
                </div>
            </div>
        </div>
            
    </section>

      <section id="start-learning">
          <div class="ms-container">
              <div class="row">
                  <div class="col-12">
                      <h5></h5>
                      <h1></h1>
                      <div class="card text-center">
                            <img src="../assets/img/home-5-image-box-01.png" class="card-img-top" alt="01">
                            <div class="card-body">
                                <h6 class="card-title">Card title</h6>
                                <p class="card-text card-font-size">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                                <a href="#" class="btn btn-light card-font-size fw-bold">Go somewhere<i class="bi bi-arrow-right ps-2"></i></a>
                            </div>
                      </div>
                  </div>
              </div>
          </div>
      </section>

      
  </main>
</template>

<script>
export default {
    name: 'mainIndex',
    data: function(){
        return {
            iconsListJumbo: ['far fa-dot-circle', 'fas fa-book', 'bi bi-cart3'],
            upHere: false,
            startLearningCards: [
                {
                    image: 'home-5-image-box-01.png',
                    title: 'Idea Discussion',
                    text: 'Get teamed up with the specialists who work and teach coding fpr years at famous universities.',
                },
                {
                    image: 'home-5-image-box-02.png',
                    title: 'Web Development',
                    text: 'Learn to start building a webpage from scratch. You decide your own pace, course and speed.',
                },
                {
                    image: 'home-5-image-box-03.png',
                    title: 'System Administration',
                    text: 'Learners are encouraged to study the mechanism and structure of system administration.',
                },
                {
                    image: 'home-5-image-box-04.png',
                    title: 'Graphic Design',
                    text: 'Have a passion for graphics and arts? Show your talents with confidence and self-assertiveness.',
                }
            ],

        }
    }

}
</script>

<style lang="scss" scoped>
@import '../assets/style/_variables.scss';

main{
    width: 100%;

    section#jumbotron{
        width: 100%;
        height: 600px;
        background-color: $brandPrimary;

        img#jumbo-overlay{
            transform: rotate(180deg);
            transform: scaleY(-1);
        }

        div.menu{
            right: 0;
            top: 90px;

            a{
                color: black;

                img{
                    width: 16px;
                }

                i{
                    font-size: 1rem;
                }
            }
        }

        div.ms-container{
            img.main-img{
                width: 500px;
            }

            h1.title{
                color: $brandColorTextPrimary;
            }

            p.content-text{
                color: $brandColorContentText;
            }

            a{
                font-size: .9rem;
                z-index: 2;
            }
        }
    }

    section#start-learning{
        height: 350px;
        background-color: yellowgreen;

        div.card{
            width: 200px;
            background-color: teal;

            img{
                width: 150px;
                margin: 0 auto;
            }

            p.card-text{
                font-size: .8rem;
            }
        }
    }
    
}

</style>