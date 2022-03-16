<template>
    <!-- header -->
      <header>
          <!-- Logo -->
          <div>
              <img  src="@/assets/Logo.png" alt="Logo food">
          </div>
          <!--/ Logo -->
          <!-- links  -->
          <nav>
              <ul class="flex flex-col justify-center justify-items-center text-center">
                  <a class="text-red-400 p-4 nav-item" href="#"><li><i class="fa-solid fa-house"></i></li></a>
                  <a class="text-red-400 p-4 nav-item" href="#"><li><i class="fa-solid fa-percent"></i></li></a>
                  <a class="text-red-400 p-4 nav-item" href="#"><li><i class="fa-solid fa-gears"></i></li></a>
                  <a class="text-red-400 p-4 nav-item" href="#"><li><i class="fa-solid fa-envelope"></i></li></a>
                  <a class="text-red-400 p-4 nav-item" href="#"><li><i class="fa-solid fa-bell"></i></li></a>
                  <a class="text-red-400 p-4 nav-item" href="#"><li><i class="fa-solid fa-arrow-right-to-bracket"></i></li></a>
              </ul>
          </nav>
          <!-- links  -->
      </header>
      <!--/ header -->
</template>

<script>
export default {
  name: "ItemNavegation",
  
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header, section{
    height: 100vh;
}
header{
    width: 5%;
}

nav ul{
    width: 100%;
    font-size: 1.8rem;
}
.nav-item{
    position: relative;
}
.nav-item:hover li:after, .nav-item:active li:after{
    content: "";
    width: 2rem;
    height: 2.65rem;
    background-color:  #393C49;
    position: absolute;
}
.nav-item:hover li, .nav-item:active li{
    background-color:  #393C49;
    border-radius: 8px 8px 8px 8px;
}

</style>
