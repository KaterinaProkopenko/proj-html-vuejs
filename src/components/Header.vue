<template>
  <header>
      <div class="ms-container">
          <div class="row">
              <div class="col-12 d-flex justify-content-between">

                  <!-- Logo -->
                  <div class="logo-container d-flex align-items-center">
                      <a href="#">
                        <img src="../assets/img/dark-logo.png" alt="Logo">
                      </a>
                  </div>

                  <div class="navbar">
                      <!-- List -->
                      <nav>
                        <a href="#" class="ms-nav ms-4" v-for="(element, index) in navbarList" :key="index">
                            {{element}}
                            <span class="fas fa-angle-down"></span>
                        </a>
                      </nav>

                      <!-- Cart -->
                      <a href="#" id="cart" class="position-relative pt-1 text-dark ms-2">
                          <i class="fas fa-shopping-cart"></i>
                          <span id="circle" class="fw-bold rounded-circle position-absolute text-light">0</span>
                      </a>

                      <!-- User -->
                      <a href="#" id="user" class="text-dark rounded-circle mx-3">
                          <i class="far fa-user"></i>
                      </a>

                      <!-- Input search -->
                      <div class="search">
                            <input type="text" class="py-2 px-3 border border-white rounded-start" placeholder="Search...">
                            <div id="icon-search" class="bg-white d-inline-block px-3 rounded-end"><i class="fas fa-search"></i></div>
                      </div>
                  </div>            
              </div>
          </div>
      </div>
  </header>
</template>

<script>
export default {
    name: 'headerIndex',
    data: function(){
        return {
            navbarList: ['Home', 'Pages', 'Courses', 'Features', 'Blog', 'Shop']
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/_variables.scss';

header{
    width: 100%;
    height: 60px;
    background-color: $brandPrimary;

    div.logo-container{

        img{
            width: 180px;
        }
    }

    div.navbar{
        a.ms-nav{
            color: $brandColorTextPrimary;

            span{
                font-size: .7rem;
            }
        }

        a#cart{
            width: 30px;

            span#circle{
                background-color: $brandColorTextSecondary;
                padding: .1rem .3rem;
                font-size: .5rem;
                right: 0;
                top: 0;
            }

        }

        a#user{
            padding: 1px 5px;
            font-size: .7rem;
            border: 1px solid black;
        }
    }

    div.search{

        input{
            width: 150px;
            outline: none;
        }

        div#icon-search{
            padding: 8.9px 0;
            color: $brandColorTextSecondary;
        }
    }
}

</style>