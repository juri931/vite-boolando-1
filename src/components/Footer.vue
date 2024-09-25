<script >



</script>



<template>

<footer>
    <div class="container-footer">
      <div class="box">
        <div class="info">
          <h4>Boolando s.r.l.</h4>
          <!-- nav -->
          <nav class="menu">
            <ul>
              <li><a href="#">Informazioni legali</a></li>
              <li><a href="#">Informativa sulla privacy</a></li>
              <li><a href="#">Diritto di recesso</a></li>
            </ul>
          </nav>
        <!-- /nav -->
        </div>

        <div class="social">
          <span>Trovaci anche su</span>
          <!-- nav -->
          <nav class="menu">
            <ul>
              <li><a href="#"><i class="fa-brands fa-square-twitter"></i></a></li>
              <li><a href="#"><i class="fa-brands fa-square-facebook"></i></a></li>
              <li><a href="#"><i class="fa-brands fa-square-instagram"></i></a></li>
              <li><a href="#"><i class="fa-brands fa-square-pinterest"></i></a></li>
              <li><a href="#"><i class="fa-brands fa-square-youtube"></i></a></li>
            </ul>
          </nav>
          <!-- /nav -->
        </div>
      </div>
    </div>
  </footer>

</template>




<style lang="scss" scoped>
@use '../assets/scss/partials/general' as *;
@use '../assets/scss/partials/variables' as *;
    
  footer {
    height: 90px;
    width: 100%;
    background-color: $bgc-footer;
  }

  .container-footer{
    color: $c-whitw;
    max-width: 1380px;
    margin: 150px auto; //da levare 300px
  }

  .box{
    display: flex;
    justify-content: space-between;
    // justify-items: center;
    align-items: center;
    height: 100%;
    padding-top: 25px;
  }


  .menu ul{
    display: flex;
    list-style: none;
    justify-content: space-between;

      a{
      color: $c-whitw;
      text-decoration: none;
      margin-right: 10px;

        &:hover {
          text-decoration: underline;
        }
      }

  }



  footer .info .menu a{
    font-size: .8rem;
  }


</style>