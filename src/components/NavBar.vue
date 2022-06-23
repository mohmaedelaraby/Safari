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

          <li class="nav-item dropdown">
            <a
              class="nav-link dropdown-toggle"
              href="#"
              id="navbarDarkDropdownMenuLink"
              role="button"
              data-bs-toggle="dropdown"
              aria-expanded="false"
            >
            <div class="search__icon__container">
                <img src="@/assets/search.svg" alt="search" class="search__icon"/>
            </div>
            
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "NavBar",
  data() {
    return {
      navItems: ["ABOUT", "PORTOFOLIO", "BLOG", "FEATURES", "PAGES", "CONTCAT"],
    };
  },
};
</script>

<style lang="scss" scoped>
@media screen and (min-width: 1024px) {
  .navbar {
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
            margin-left: 40px;
            .search__icon__container{
                width: 100%;
                height: 100%;
                display: flex;
                align-items: center;
                justify-content: center;
                background-color: gray;
                .search__icon{
                  height: 20px;
          transition: 0.5s ease all;

          @media (max-width: 426px) {
            width: 90%;
            height: 30px;
          }
            }
            }
            
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
</style>
