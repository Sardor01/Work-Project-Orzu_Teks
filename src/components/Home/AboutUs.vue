<template>
  <div id="aboutUs" class="container">
    <div class="row justify-content-between my-lg-4 my-md-3 my-1 py-lg-2 py-1">
      <div
        class="col-md-5 d-flex justify-content-center align-items-end order-md-1 order-2"
      >
        <img
          src="../../assets/AboutUsMain.png"
          class="my-5 about__img"
          alt="Image 1"
        />
      </div>
      <div class="col-md-7 justify-content-start my-4 order-md-2 order-1">
        <h1 class="text-uppercase section__title mb-4">О Нас</h1>

        <p class="about__text">
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aliquid
          cumque numquam aperiam ducimus non, sint perferendis beatae vitae nisi
          voluptas qui, quis consectetur modi. Fuga minus ea modi, perspiciatis
          suscipit cumque accusamus explicabo rem, quos alias laborum totam
          beatae illum?
        </p>

        <ol class="custom_ol">
          <li data-icon="1">ПРОИЗВОДСТВО ПОЛОТНА</li>
          <li data-icon="2">ПРОИЗВОДСТВО УНИФОРМЫ</li>
          <li data-icon="3">ПРОИЗВОДСТВО ТКАНИ</li>
        </ol>

        <div class="mt-4">
          <CustomLink
            link="#"
            className="text-center d-inline-block"
            text="Подробнее"
          />
        </div>
      </div>
    </div>

    <div class="my-5 py-3">
      <!-- Tab links -->
      <div class="tabs">
        <button
          :key="idx"
          v-for="(tab, idx) in tabNames"
          class="tab col-lg-2 col-md-3 col-4"
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
          class="col-lg-3 col-md-4 col-6 mb-4 tab__content aboutUs__tab"
        >
          <div
            class="position-relative overflow-hidden text-center text-uppercase d-flex justify-content-center align-items-center"
          >
            <img :src="content.img" class="tab__img" alt="" />
            <div class="tab__text">{{ content.name }}</div>
            <div class="tab__opacity"></div>
          </div>
        </div>
      </div>

      <div class="d-flex justify-content-center mt-4">
        <CustomLink
          link="#"
          className="text-center d-inline-block"
          text="Посмотреть все"
        />
      </div>
    </div>
  </div>
</template>

<script>
  import CustomLink from "@/components/CustomLink";

  export default {
    name: "AboutUs",
    components: {
      CustomLink,
    },
    data() {
      return {
        activeTab: "",
        tabContent: [],
        tabNames: ["Полотно", "Ткани"],
        tabs: [
          {
            id: 1,
            tabName: "Полотно",
            tabContent: [
              {
                id: 1,
                img:
                  "https://images.unsplash.com/photo-1600727335606-1bb400010909?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixlib=rb-1.2.1&q=80&w=200",
                name: "lorem ipsum",
              },
              {
                id: 2,
                img:
                  "https://images.unsplash.com/photo-1602029232568-f760a7ba9687?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixlib=rb-1.2.1&q=80&w=200",
                name: "Lorem, ipsum",
              },
              {
                id: 3,
                img:
                  "https://images.unsplash.com/photo-1602126282340-9f597c2f31ab?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixlib=rb-1.2.1&q=80&w=200",
                name: "dolor sit.",
              },
              {
                id: 4,
                img:
                  "https://images.unsplash.com/photo-1602003472234-6a9fde86a446?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixlib=rb-1.2.1&q=80&w=200",
                name: "dolor sit.",
              },
              {
                id: 5,
                img:
                  "https://images.unsplash.com/photo-1601275225755-f6a6c1730cb1?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixlib=rb-1.2.1&q=80&w=200",
                name: "dolor sit.",
              },
              {
                id: 6,
                img:
                  "https://images.unsplash.com/photo-1600738845409-a5648c9e6c57?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixlib=rb-1.2.1&q=80&w=200",
                name: "dolor sit.",
              },
              {
                id: 7,
                img:
                  "https://images.unsplash.com/photo-1602796098127-16c89a59b208?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixlib=rb-1.2.1&q=80&w=200",
                name: "dolor sit.",
              },
              {
                id: 8,
                img:
                  "https://images.unsplash.com/photo-1602346097826-6cb12939074c?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixlib=rb-1.2.1&q=80&w=200",
                name: "dolor sit.",
              },
            ],
          },
          {
            id: 2,
            tabName: "Ткани",
            tabContent: [
              {
                id: 1,
                img:
                  "https://images.unsplash.com/photo-1601396773761-4cae1fff7a00?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixlib=rb-1.2.1&q=80&w=200",
                name: "lorem ipsum",
              },
              {
                id: 2,
                img:
                  "https://images.unsplash.com/photo-1600761603517-64bcda5b0163?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixlib=rb-1.2.1&q=80&w=200",
                name: "Lorem, ipsum",
              },
              {
                id: 3,
                img:
                  "https://images.unsplash.com/photo-1602646993760-7b885ba225af?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixlib=rb-1.2.1&q=80&w=200",
                name: "dolor sit.",
              },
              {
                id: 4,
                img:
                  "https://images.unsplash.com/photo-1603037738996-a04f1c6a9ce6?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixlib=rb-1.2.1&q=80&w=200",
                name: "dolor sit.",
              },
              {
                id: 5,
                img:
                  "https://images.unsplash.com/photo-1601925051520-ea55b6ffd2b0?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixlib=rb-1.2.1&q=80&w=200",
                name: "dolor sit.",
              },
              {
                id: 6,
                img:
                  "https://images.unsplash.com/photo-1601696004236-391e81b4ba9e?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixlib=rb-1.2.1&q=80&w=200",
                name: "dolor sit.",
              },
              {
                id: 7,
                img:
                  "https://images.unsplash.com/photo-1601028093469-ddbe77d537f6?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixlib=rb-1.2.1&q=80&w=200",
                name: "dolor sit.",
              },
              {
                id: 8,
                img:
                  "https://images.unsplash.com/photo-1600673406582-a41d4fa94e0c?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixlib=rb-1.2.1&q=80&w=200  ",
                name: "dolor sit.",
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