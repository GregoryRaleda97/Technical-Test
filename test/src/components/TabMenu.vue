<template>
  <div id="app">
    <tabs
      :tabs="tabs"
      :currentTab="currentTab"
      :wrapper-class="'default-tabs'"
      :tab-class="'default-tabs__item'"
      :tab-active-class="'default-tabs__item_active'"
      :line-class="'default-tabs__active-line'"
      @onClick="handleClick"
    />
    <div class="content">
      <div v-if="currentTab === 'discover-a'">
        <img
          src="@/assets/img/illustrations/addresses_contacts.jpg"
          class="mt-8 md:mt-8 md:flex-row items-center"
        />
        <div>
          Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium
          doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore
          veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam
          voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia
          consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt.
        </div>
      </div>
      <div v-if="currentTab === 'discover-b'">
        <img
          src="@/assets/img/illustrations/wallet_phone.jpg"
          class="mt-8 md:mt-8 md:flex-row items-center"
        />
        <div>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
          incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
          nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
          Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu
          fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
          culpa qui officia deserunt mollit anim id est laborum.
        </div>
      </div>
      <div v-if="currentTab === 'discover-c'">
        <img
          src="@/assets/img/illustrations/instant_payments.jpg"
          class="mt-8 md:mt-8 md:flex-row items-center"
        />
        <div>
          At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis
          praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias
          excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui
          officia deserunt mollitia animi, id est laborum et dolorum fuga.
        </div>
      </div>
      <div v-if="currentTab === 'discover-d'">
        <img
          src="@/assets/img/illustrations/open_source.jpg"
          class="mt-8 md:mt-8 md:flex-row items-center"
        />
        <div>
          Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium
          doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore
          veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam
          voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia
          consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt.
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Tabs from "vue-tabs-with-active-line";
const TABS = [
  {
    title: "Discover A",
    value: "discover-a",
  },
  {
    title: "Discover B",
    value: "discover-b",
  },
  {
    title: "Discover C",
    value: "discover-c",
  },
  {
    title: "Discover D",
    value: "discover-d",
  },
];
export default {
  components: {
    Tabs,
  },
  data: () => ({
    tabs: TABS,
    currentTab: "discover-a",
  }),
  methods: {
    handleClick(newTab) {
      this.currentTab = newTab;
    },
  },
};
</script>

<style lang="scss">
.default-tabs {
  position: relative;
  margin: 0 auto;
  &__item {
    display: inline-block;
    margin: 0 5px;
    padding: 10px;
    padding-bottom: 8px;
    font-size: 16px;
    letter-spacing: 0.8px;
    color: gray;
    text-decoration: none;
    border: none;
    background-color: transparent;
    border-bottom: 2px solid transparent;
    cursor: pointer;
    transition: all 0.25s;
    &_active {
      color: black;
    }
    &:hover {
      border-bottom: 2px solid gray;
      color: black;
    }
    &:focus {
      outline: none;
      border-bottom: 2px solid gray;
      color: black;
    }
    &:first-child {
      margin-left: 0;
    }
    &:last-child {
      margin-right: 0;
    }
  }
  &__active-line {
    position: absolute;
    bottom: 0;
    left: 0;
    height: 4px;
    background-color: rgb(88, 0, 0);
    transition: transform 0.4s ease, width 0.4s ease;
  }
}
.content {
  margin-top: 30px;
  font-size: 20px;
}
</style>
