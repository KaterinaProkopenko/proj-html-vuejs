<template>
  <footer class="bg-white">
      <div class="ms-container">
        <div class="row pt-5 pb-4 px-5">

          <!-- Address -->
          <div class="col-6 pb-5 ps-5">
            <h6 class="fw-bold mb-3">Address</h6>
            <p class="text-size mb-3" v-for="(element, index) in address" :key="index">{{element}}</p>

            <!-- Icons -->
            <div class="footer-icons fs-5">
              <a v-for="(element, index) in icons" :key="index" href="#">
                <i :class="element" class="me-4"></i>
              </a>
              
            </div>
          </div>

          <!-- Explore and Information lists-->
          <div class="col-6 d-flex">

            <!-- Explore list -->
            <ul>
              <h6 class="fw-bold mb-3">Explore</h6>
              <li v-for="(element, index) in exploreList" :key="index" class="pb-2">
                <a href="#" class="text-size">{{element}}</a>
              </li>
            </ul>

            <!-- Center list -->
            <ul class="center-list ps-5">
              <li v-for="(element, index) in list" :key="index" class="pb-2">
                <a href="#" class="text-size">{{element}}</a>
              </li>
            </ul>

            <!-- Information list -->
            <ul class="ps-5">
              <h6 class="fw-bold mb-3">Information</h6>
              <li v-for="(element, index) in informationList" :key="index" class="pb-2">
                <a href="#" class="text-size">{{element}}</a>
              </li>
            </ul>
          </div>

          <div class="col-12">
            <p class="text-size fw-bold text-center">&copy; 2020 Maxcoach. All Rights Reserveds</p>
          </div>
        </div>
      </div>
  </footer>
</template>

<script>
export default {
    name: 'footerIndex',
    data: function(){
      return{
        address: ['382 NE 191st St # 87394 Miami, FL 33179-3899', '+1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)', 'support@maxcoach.com'],
        icons: ['fab fa-facebook-square', 'fab fa-twitter', 'fab fa-instagram', 'fab fa-linkedin'],
        exploreList: ['Start here', 'Blog', 'About us'],
        list: ['Success story', 'Courses', 'Contact us'],
        informationList: ['Membership', 'Purchase guide', 'Privacy policy', 'Terms of services']
      }
    }

}
</script>

<style lang="scss" scoped>
@import "../assets/style/_variables.scss";

footer{
  div.footer-icons{
    i{
      color: $brandColorContentText; 
    }
  }

  ul.center-list{
    padding-top: 35.2px;
  }

  a:hover{
    color: $brandColorContentText;
  }
}

</style>