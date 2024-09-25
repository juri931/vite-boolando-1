<script >

export default {
  data(){
    return {
        mainMenu: [
          {
            tipo: 'donna',
            link: '#'
          },
          {
            tipo: 'uomo',
            link: '#'
          },
          {
            tipo: 'bambini',
            link: '#'
          },
        ],
        socialMenu: [
          {
            icon: '<i class="fa-regular fa-user"></i>',
            link: '#'
          },
          {
            icon: '<i class="fa-regular fa-heart"></i>',
            link: '#'
          },
          {
            icon: '<i class="fa-solid fa-bag-shopping"></i>',
            link: '#'
          },
        ]

      


    }
  }
}

</script>



<template>

  <header>
      <div class="container-header ">
        <div class="row justify-beetween align-center  ">
          <div class="col ">
            <nav>
              <ul class="main-menu">
                <li 
                v-for="(element, index) in mainMenu" 
                :key="`m-${index}`">
                  <a :href="element.link">{{ element.tipo }}</a>
                </li>
            
              </ul>
            </nav>
          </div>
          <div class="col logo ">
            <img src="../assets/img/boolean-logo.png" alt="Logo">
          </div>

          <div class="col ">
            <nav>

              <ul class="social-menu">
                <li 
                v-for="(elemento, index) in socialMenu"
                :key="`s-${index}`">
                  <a 
                  :href="elemento.link" 
                  v-html="elemento.icon">
                </a>
                </li>                
              </ul>

            </nav>
          </div>

        </div>
      </div>
    </header>

</template>




<style lang="scss" scoped>
@use '../assets/scss/partials/general' as *;
@use '../assets/scss/partials/variables' as *;

  header {
    position: fixed;
    z-index: 999;
    width: 100%;
    height: 80px;
    background-color: $bgc-header;
    box-shadow: 0 1px 3px rgba(128, 128, 128, 0.896);
    top: 0;
  }

  .container-header {
    width: 98%;
    max-width: 1380px;
    margin: 0 auto;
    height: 100%;
  }

  .row {
    display: flex;
    flex-wrap: wrap;
    height: 100%;
  }

  .col {
    width: calc(100% / 3);
    padding: 0 10px;
  }

.main-menu {
    display: flex;
    list-style: none;

    a {
      color: $c-whitw;
      text-transform: capitalize;
      text-decoration: none;
      padding-right: 15px;
      font-weight: 700;

        &:hover {
          text-decoration: underline;
        }
    }
  }

  
.social-menu {
    display: flex;
    list-style: none;
    justify-content: flex-end;

      a {
      color: $c-whitw;
      text-transform: capitalize;
      text-decoration: none;
      padding-right: 15px;
      padding: 0 3px;
    }

  }


  header .logo {
    width: 170px;
    padding-top: 15px;
  }

  img {
    width: 100%;
  }


</style>