<template>
  <div class="menu-item">
    <div class="menu-head" @click="toggleSubmenu">
      <i class="fa-solid fa-building menu-icon"></i>
      &nbsp;
      <div class="item-name">This is a Store Icon</div>
      <i class="fa-solid fa-caret-down down-arrow-icon" v-if="showsubmenu"></i>
      <i class="fa-solid fa-caret-right down-arrow-icon"></i>
    </div>

    <!-- Sub-Menu -->
    <div class="sub-menu-item" v-if="showsubmenu">
      <div class="sub-item-head">
        <i class="fa-solid fa-building submenu-icon"></i>
        &nbsp;
        <div class="item-name">Sub Menu Item</div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      showsubmenu: false,
      submenuarrow: "",
    };
  },
  methods: {
    toggleSubmenu() {
      this.showsubmenu = !this.showsubmenu;
    },
  },
};
</script>
<style scoped>
.menu-item {
  position: relative;
  display: block;
  height: fit-content;
  left: 0px;
  width: 100%;
}

.menu-head {
  position: relative;
  display: block;
  height: 30px;
  color: var(--theme-color);
  font-size: 14px;
  left: 0px;
  width: 100%;
  padding: 5px;
}

.menu-head:hover {
  cursor: pointer;
  background-color: var(--theme-color);
  color: white;
}

.menu-head .menu-icon {
  position: relative;
  display: inline-block;
  font-size: 23px;
  color: var(--theme-color);
  top: 2px;
  left: 8px;
}

.menu-head .down-arrow-icon {
  position: relative;
  font-size: 12px;
  text-align: right;
  margin-left: 25px;
}

.menu-head .item-name {
  position: relative;
  display: inline-block;
  font-weight: 500;
  top: 0px;
  left: 15px;
}

.menu-head:hover .menu-icon {
  color: white;
}

.sub-menu-item {
  position: relative;
  display: block;
  cursor: pointer;
  left: 0px;
  padding: 8px;
  font-size: 14px;
  width: 100%;
  color: var(--theme-color);
}

.sub-menu-item:hover {
  background-color: var(--theme-color);
  color: white;
}

.sub-menu-item .item-name {
  position: relative;
  display: inline-block;
  font-weight: 500;
  top: 0px;
  left: 15px;
}
.sub-menu-item .sub-item-head {
  padding: 2px;
}
</style>
