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
@import '@/assets/styles/compnonets/NavBar.scss'
</style>
