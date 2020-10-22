<template>
  <div id="collection" class="container my-5 py-2">
    <h1 class="text-center text-uppercase section__title">Коллекция</h1>

    <div class="my-5 py-3">
      <!-- Tab links -->
      <div class="tabs">
        <button
          :key="idx"
          v-for="(tab, idx) in tabNames"
          class="tab"
          :class="{ active: activeTab === tab }"
          @click="OpenTab(tab)"
        >
          {{ tab }}
        </button>
      </div>

      <!-- Tab content -->
      <div class="row mt-4 justify-content-center">
        <div
          :key="content.id"
          v-for="content in tabContent"
          class="col-lg-4 col-6 mb-3 text-center tab__content collection__tab"
        >
          <div class="position-relative overflow-hidden">
            <img :src="content.img" class="w-100" alt="" />
            <div class="tab__imgText">{{ content.name }}</div>
            <div class="tab__opacity"></div>
          </div>
        </div>
      </div>

      <div class="d-flex justify-content-center mt-4">
        <CustomButton
          className="text-center d-inline-block"
          text="Посмотреть все"
        />
      </div>
    </div>
  </div>
</template>

<script>
  import CustomButton from "@/components/CustomButton";

  export default {
    name: "Collection",
    components: {
      CustomButton,
    },
    data() {
      return {
        activeTab: "",
        tabContent: [],
        tabNames: ["Детская", "Мужская", "Женская"],
        tabs: [
          {
            id: 1,
            tabName: "Детская",
            tabContent: [
              {
                id: 1,
                img:
                  "https://images.unsplash.com/photo-1601843488865-c2a35baa216f?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=350&ixlib=rb-1.2.1&q=80&w=350",
                name: "lorem ipsum",
              },
              {
                id: 2,
                img:
                  "https://images.unsplash.com/photo-1603137498553-cbb1817cad74?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=350&ixlib=rb-1.2.1&q=80&w=350",
                name: "lorem ipsum",
              },
              {
                id: 3,
                img:
                  "https://images.unsplash.com/photo-1601433864910-28e7ea4c9c8b?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=350&ixlib=rb-1.2.1&q=80&w=350",
                name: "lorem ipsum",
              },
              {
                id: 4,
                img:
                  "https://images.unsplash.com/photo-1602933542414-63ef186251c6?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=350&ixlib=rb-1.2.1&q=80&w=350",
                name: "lorem ipsum",
              },
              {
                id: 5,
                img:
                  "https://images.unsplash.com/photo-1601461431175-30631903a66c?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=350&ixlib=rb-1.2.1&q=80&w=350",
                name: "lorem ipsum",
              },
              {
                id: 6,
                img:
                  "https://images.unsplash.com/photo-1601393656243-a3a71b7ce4d7?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=350&ixlib=rb-1.2.1&q=80&w=350",
                name: "lorem ipsum",
              },
            ],
          },
          {
            id: 2,
            tabName: "Мужская",
            tabContent: [
              {
                id: 1,
                img:
                  "https://images.unsplash.com/photo-1603039826911-aed407e02f2e?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=350&ixlib=rb-1.2.1&q=80&w=350",
                name: "lorem ipsum",
              },
              {
                id: 2,
                img:
                  "https://images.unsplash.com/photo-1602710497677-3fcf173df0b9?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=350&ixlib=rb-1.2.1&q=80&w=350",
                name: "lorem ipsum",
              },
              {
                id: 3,
                img:
                  "https://images.unsplash.com/photo-1601832681088-fd4d458878eb?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=350&ixlib=rb-1.2.1&q=80&w=350",
                name: "lorem ipsum",
              },
              {
                id: 4,
                img:
                  "https://images.unsplash.com/photo-1600933650113-e40890fcdcb0?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=350&ixlib=rb-1.2.1&q=80&w=350",
                name: "lorem ipsum",
              },
              {
                id: 5,
                img:
                  "https://images.unsplash.com/photo-1600998837340-4887228e311f?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=350&ixlib=rb-1.2.1&q=80&w=350",
                name: "lorem ipsum",
              },
              {
                id: 6,
                img:
                  "https://images.unsplash.com/photo-1602549118289-e1572491fe0a?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=350&ixlib=rb-1.2.1&q=80&w=350",
                name: "lorem ipsum",
              },
            ],
          },
          {
            id: 3,
            tabName: "Женская",
            tabContent: [
              {
                id: 1,
                img:
                  "https://images.unsplash.com/photo-1600934258627-aa83a8ad1dd2?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=350&ixlib=rb-1.2.1&q=80&w=350",
                name: "lorem ipsum",
              },
              {
                id: 2,
                img:
                  "https://images.unsplash.com/photo-1601586063627-4fd8dff4dc28?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=350&ixlib=rb-1.2.1&q=80&w=350",
                name: "lorem ipsum",
              },
              {
                id: 3,
                img:
                  "https://images.unsplash.com/photo-1603094625062-15d05e847711?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=350&ixlib=rb-1.2.1&q=80&w=350",
                name: "lorem ipsum",
              },
              {
                id: 4,
                img:
                  "https://images.unsplash.com/photo-1603024251143-4fefa9caac5a?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=350&ixlib=rb-1.2.1&q=80&w=350",
                name: "lorem ipsum",
              },
              {
                id: 5,
                img:
                  "https://images.unsplash.com/photo-1602704001252-6a56b9291171?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=350&ixlib=rb-1.2.1&q=80&w=350",
                name: "lorem ipsum",
              },
              {
                id: 6,
                img:
                  "https://images.unsplash.com/photo-1602139299155-431bac10fea7?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=350&ixlib=rb-1.2.1&q=80&w=350",
                name: "lorem ipsum",
              },
            ],
          },
        ],
      };
    },
    methods: {
      OpenTab(tab) {
        this.tabs.forEach((t) => {
          if (tab === t.tabName) {
            this.activeTab = t.tabName;
            this.tabContent = t.tabContent;
          }
        });
      },
    },
    created() {
      this.tabContent = this.tabs[0].tabContent;
      this.activeTab = this.tabs[0].tabName;
    },
  };
</script>

<style>
</style>