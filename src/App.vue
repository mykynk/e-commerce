<template>
  <div id="app">
    <nav class="navbar navbar-dark bg-dark navbar-expand-lg  ">
      <div class="container-fluid" style="justify-content: center; align-items: center" >
        <a class="navbar-brand sec"  href="#" style="position: absolute; left: 20px" >Arif Tic</a   >
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation" >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="center navbar-center " id="navbarNav">
          <ul class="navbar-nav  " >
            <li class="nav-item" >
              <a  class="nav-link active  sec arrow"  aria-current="page"  href="#"  >Home</a>
            </li>
            <li class="nav-item">
              <a class="nav-link sec arrow" href="#">Features</a>
            </li>
            <li class="nav-item ">
              <a class="nav-link sec arrow" href="#">Pricing</a>
            </li>
            <li class="nav-item">
              <a class="nav-link sec arrow" href="#">Disabled</a>
            </li>
          </ul>
        </div>    
      </div>
      <form class="d-flex ">
        <input class="form-control me-2 arama " type="search" placeholder="Ara" aria-label="Ara" style="height:25px ">
        <button class="btn btn-outline-dark btn arama" type="submit">Ara</button>
        <button class="btnsepetim" type="submit">Sepetim</button>

      </form>
    </nav>
    <router-view />
    
  </div>
</template>
<script>
export default {
  name: "App",

  data() {
    return {
      upHere: true,
    };
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
 
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
.buyutec {
  position: relative;
  -webkit-transform: scale(1);
  -ms-transform: scale(1);
  -moz-transform: scale(1);
  transition: all 0.3s ease-in;
  -moz-transition: all 0.3s ease-in;
  -webkit-transition: all 0.3s ease-in;
  -ms-transition: all 0.2s ease-in;
}
.buyutec:hover {
  z-index: 4;
  -webkit-transform: scale(1.2);
  -ms-transform: scale(1.2);
  -moz-transform: scale(1.2);
  transform: scale(1.2);
}
.sec {
  display: inline-block;
  position: relative;
  padding-bottom: 3px;
  left: 100px;
}
.sec:after {
  content: "";
  display: block;
  margin: auto;
  height: 2px;
  width: 0px;
  background: transparent;
  transition: width 0.5s ease, background-color 0.5s ease;
  border-radius: 60px;
}
.sec:hover:after {
  width: 90%;
  background: white;
}

.up {
  overflow: hidden;
  position: relative;
}
.up:after {
  bottom: 0%;
  color: #fff;
  height: 100%;
  transition: bottom 0.5s ease;
  width: 100%;
}
.up:hover:after{
  bottom: 10%;
}
.arrow {
  position: relative;
  top: 0;
  transition: top ease 0.5s;
}
.arrow:hover {
  top: -5px;
}
.arama {
  display: inline-block;
  position: relative;
  padding-bottom: 3px;
  right: 15px;
 
}
.btn {
    text-align: center;
    font-size: 0.6em;
    height: 25px;
    text-transform: uppercase;
    background: white;
    padding: 1em 0.6em;
    color:black;
    line-height: 2px; 
}
.btnsepetim {
  display: inline-block;
  position: relative;
  background: #ffffff;
  background-image: -webkit-linear-gradient(top, #ffffff, #ffffff);
  background-image: -moz-linear-gradient(top, #ffffff, #ffffff);
  background-image: -ms-linear-gradient(top, #ffffff, #ffffff);
  background-image: -o-linear-gradient(top, #ffffff, #ffffff);
  background-image: linear-gradient(to bottom, #ffffff, #ffffff);
  -webkit-border-radius: 11;
  -moz-border-radius: 11;
  border-radius: 7px;
  color: #000000;
  font-size: 11px;
  padding: 3px 3px 4px 4px;
  border: solid #000000 2px;
  text-decoration: none;
  right:10px
}

.btnsepetim:hover {
  background: #000000;
  text-decoration: none;
  color: #fff;
}
</style>
