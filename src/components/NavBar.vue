<template>
  <nav class="navbar navbar-expand-lg">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">
        <div class="logo">
          <img src="@/assets/Safari.svg" alt="logo" />
        </div>
      </a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNavDarkDropdown"
        aria-controls="navbarNavDarkDropdown"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavDarkDropdown">
        <ul class="navbar-nav">
          <li class="nav-item dropdown">
            <a
              class="nav-link dropdown-toggle"
              href="#"
              id="navbarDarkDropdownMenuLink"
              role="button"
              data-bs-toggle="dropdown"
              aria-expanded="false"
            >
              HOME
            </a>
            <div class="dropdown">
              <ul class="dropdown-menu" aria-labelledby="dropdownMenu2">
                <li>
                  <button class="dropdown-item" type="button">
                    Home Portfolio
                  </button>
                </li>
                <hr />
                <li>
                  <button class="dropdown-item" type="button">
                    Home Portfolio
                  </button>
                </li>
                <hr />
                <li>
                  <button class="dropdown-item" type="button">
                    Home Portfolio
                  </button>
                </li>
              </ul>
            </div>
          </li>

          <li
            class="nav-item dropdown"
            v-for="(item, index) in navItems"
            v-bind:key="index"
          >
            <a
              class="nav-link dropdown-toggle"
              href="#"
              id="navbarDarkDropdownMenuLink"
              role="button"
              data-bs-toggle="dropdown"
              aria-expanded="false"
            >
              {{ item }}
            </a>
          </li>
        </ul>
      </div>
    </div>

    <div class="search__icon__container" @click="active=true">
    
    <input  v-if="active" :class="{ 'input__active': 'input__not__active' }"  placeholder="Search ..." @keyup.enter="active=false"/>
      <img src="@/assets/search.svg" alt="search" class="search__icon" />
    </div>
  </nav>
</template>

<script>
export default {
  name: "NavBar",
  data() {
    return {
      navItems: ["ABOUT", "PORTOFOLIO", "BLOG", "FEATURES", "PAGES", "CONTCAT"],
      active:false
    };
  },
};
</script>

<style lang="scss" scoped>
@media screen and (min-width: 1024px) {
  .navbar {
    padding: 0px;
    height: 8vh;

    .search__icon__container {
      display: flex;
      align-items: center;
      justify-content: center;
      background-color: rgb(233, 232, 232);
      height: 100%;
      width: 7%;
      cursor: pointer;
   

     .input__not__active{
        border: none;
        right: 0;
        width: 0;
        
     }
     .input__active{
        border: 1px solid black;
        border-top-left-radius: 50px;
          border-bottom-left-radius: 50px;
        position: absolute;
        right: 0;
        height: 100%;
        width: 80%;
        outline: none;
        font-size: 25px;
         transition: 0.5s ease-in all;
     }

      .search__icon {
        height: 20px;
      }
    }
    .container-fluid {
      padding: 0px;
      .navbar-brand {
        margin-left: 100px;
        .logo {
          display: flex;
          align-items: center;
          cursor: pointer;

          img {
            width: 100%;
            height: 35px;
            transition: 0.5s ease all;

            @media (max-width: 426px) {
              width: 90%;
              height: 30px;
            }
          }
        }
      }

      .collapse {
        justify-content: space-around;

        .navbar-nav {
          width: 100%;
          display: flex;
          justify-content: flex-end;
          .nav-item {
            margin-right: 40px;
            .nav-link {
              color: grey;
              font-weight: 500;
              font-style: 14px;
              &:hover {
                transition: 0.2s ease-in-out;
                color: aqua;
              }
            }
          }

          .dropdown {
            &:hover {
              .dropdown-menu {
                display: block;
                margin-top: 0;
                border-radius: 0;
                hr {
                  color: gray;
                  margin-left: 5px;
                  margin-right: 5px;
                }
                li {
                  margin-bottom: 18px;
                }
                .dropdown-item {
                  color: gray;
                  transition: 0.2s ease-in-out;
                  padding-left: 34px;
                  padding-right: 47px;
                  padding-top: 8px;

                  &:hover {
                    background-color: white;
                    transition: 0.2s ease-in-out;
                    color: aqua;
                  }
                }
              }
            }
          }
        }
      }
    }
  }
}
@media screen and (max-width: 770px) {
    .search__icon__container{
        display: flex;
        align-items: center;
        justify-content: flex-end;
        background-color: red;
        width: 100%;
        height: 40px;
        .search__icon {
        height: 20px;
        margin-right: 25px;
      }
    }
}
</style>
