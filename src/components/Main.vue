<template>
  <main class="position-relative">

      <section id="jumbotron">
            <!-- Jumbo overlay -->
            <img id="jumbo-overlay" class="w-100 h-50 position-absolute bottom-0" src="../assets/img/jumbo-overlay.svg" alt="jumbo-overlay">

            <!-- Right menu -->
            <div class="menu position-absolute d-flex flex-column bg-light p-2 pt-0 gap-3 rounded">
                <a href="#">
                    <img src="https://www.kindpng.com/picc/m/34-346527_ruler-triangle-drafting-triangle-icon-png-transparent-png.png" alt="ruler">
                </a>
                <a href="#" v-for="(element, index) in iconsList" :key="index">
                    <i :class="element"></i>
                </a>
            </div>

            <div class="ms-container">
                <div class="row">

                    <!-- Left content -->
                    <div class="col-5 py-4 pe-5">
                        <h1 class="title fw-bold mt-5 pt-3">Complete Your Dreams in JavaS Programming</h1>
                        <p class="content-text py-2">Learn any coding program in distance and for a reasonable fee. You don't have to struggle alone, you've got our assistence and help.</p>
                        <button type="button" class="btn btn-primary"><i class="fas fa-download"></i>Download free E-book</button>
                    </div>

                    <!-- Right image -->
                    <div class="col-7 pt-4 text-end">
                        <img class="main-img" src="../assets/img/home-5-hero-image.png" alt="Home hero image">
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
            iconsList: ['far fa-dot-circle', 'fas fa-book', 'bi bi-cart3']
        }
    }

}
</script>

<style lang="scss" scoped>
@import '../assets/style/_variables.scss';

main{
    width: 100%;
    height: 600px;
    background-color: $brandPrimary;

    section#jumbotron{

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

            button{
                background-color: $brandColorTextSecondary;
                border: 1px solid $brandColorTextSecondary;
            }
        }
    }

    
}

</style>