<template>
  <div class="row" style="margin: 0px">
    <section>
      <div class="row">
        <div class="col-xl-12">
          <div class="header">
            <h2>OUR PORTFOLIO</h2>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit aliquam at
              libero justo maecenas nibh tortor, mollis ac arcu vitae.
            </p>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-xl-12">
          <div class="filter_buttons">
            <button
              v-for="(item, index) in listofbutton"
              v-bind:key="index"
              @click="filterPosts(item)"
            >
              {{ item }}
            </button>
          </div>
        </div>
      </div>
      <div class="row">
          <div class="container">
            <FilterCard
              v-for="item in posts"
              v-bind:key="item.id"
              :header="item.title"
              :src="item.img"
              :txt="item.txt"
            />
          </div>
      </div>
    </section>
  </div>
</template>

<script>
import ddata from "../Filteretion/data";
import FilterCard from "./FilterCard.vue";
export default {
  data() {
    return {
      listofbutton: [
        "ALL",
        "ILLUSTRATION",
        "PHOTOGRAPHY",
        "DESIGN",
        "WALLPAPER",
      ],
      posts: ddata,
    };
  },
  setup() {
    return {};
  },
  methods: {
    filterPosts(catName) {
      this.resetPosts();
      if (catName !== "ALL") {
        this.posts = this.posts.filter((post) => {
          return post.txt.toUpperCase() === catName;
        });
      }
    },
    resetPosts() {
      this.posts = ddata;
    },
  },
  components: { FilterCard },
};
</script>

<style lang="scss" scoped>
section {
  background-color: #f4f4f4;
  .row {
    .col-xl-12 {
      display: flex;
      justify-content: center;
      .header {
        margin-top: 100px;
        margin-bottom: 100px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        h2 {
          margin-bottom: 50px;
          font-weight: 600;
        }
        p {
          width: 80%;
        }
      }
      .filter_buttons {
        width: 80%;

        margin-bottom: 100px;
        display: flex;
        justify-content: center;
        button {
          cursor: pointer;
          border: 1px solid gray;
          background-color: transparent;
          margin-left: 7px;
          font-size: 14px;
          padding: 6px;
          padding-left: 15px;
          padding-right: 15px;
          color: #686868;
          &:hover {
            color: #5cc8c5;
            border: 1px solid #5cc8c5;
          }
        }
      }
  
    }

        .container{
        display: flex;
        flex-wrap: wrap;
        width: 100%;
        align-items: center;
        justify-content: center;
      }
  }
}
</style>
