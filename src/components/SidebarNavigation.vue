<script setup>

</script>

<template>
  <div class="navigation-menu bg-white rounded-md w-[360px] p-4 mt-6">
    <ul class="flex flex-col gap-6">
      <li>
        <router-link class="flex items-center gap-3" to="/">
          <img src="../assets/img/icons/square.svg" alt="square">
          Плитные материалы
        </router-link>
      </li>
      <li>
        <router-link class="flex items-center gap-3" to="/">
          <img src="../assets/img/icons/case.svg" alt="case">
          Мебельная фурнитура
        </router-link>
      </li>
      <li>
        <router-link class="flex items-center gap-3" to="/">
          <img src="../assets/img/icons/floor.svg" alt="floor">
          Столешницы и стенпанели
        </router-link>
      </li>
      <li>
        <router-link class="flex items-center gap-3" to="/">
          <img src="../assets/img/icons/brick.svg" alt="brick">
          Фасады
        </router-link>
      </li>
      <li>
        <router-link class="flex items-center gap-3" to="/">
          <img src="../assets/img/icons/wardrobe.svg" alt="wardrobe">
          Дверные и гардеробные системы
        </router-link>
      </li>
      <li>
        <router-link class="flex items-center gap-3" to="/">
          <img src="../assets/img/icons/mirror.svg" alt="mirror">
          Стекло и зеркало
        </router-link>
      </li>
      <li>
        <router-link class="flex items-center gap-3" to="/">
          <img src="../assets/img/icons/furniture.svg" alt="furniture">
          Мебель
        </router-link>
      </li>
      <li>
        <router-link class="flex items-center gap-3" to="/">
          <img src="../assets/img/icons/desk-lamp.svg" alt="desk-lamp">
          Освещение для мебели
        </router-link>
      </li>
      <li>
        <router-link class="flex items-center gap-3" to="/">
          <img src="../assets/img/icons/appliance.svg" alt="appliance">
          Бытовая техника
        </router-link>
      </li>
      <li>
        <router-link class="flex items-center gap-3" to="/">
          <img src="../assets/img/icons/stone.svg" alt="stone">
          Изделия из камня
        </router-link>
      </li>
      <li>
        <router-link class="flex items-center gap-3" to="/">
          <img src="../assets/img/icons/metal.svg" alt="metal">
          Изделия из метала
        </router-link>
      </li>
      <li>
        <router-link class="flex items-center gap-3" to="/">
          <img src="../assets/img/icons/parquet.svg" alt="parquet">
          Напольные покрытия
        </router-link>
      </li>
      <li>
        <router-link class="flex items-center gap-3" to="/">
          <img src="../assets/img/icons/tools.svg" alt="tools">
          Инструменты и расходные материалы
        </router-link>
      </li>
      <li>
        <router-link class="flex items-center gap-3" to="/">
          <img src="../assets/img/icons/manufacturing.svg" alt="manufactoring">
          Производственные услуги
        </router-link>
      </li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
.navigation-menu {
  ul {
    li {
      color: #212121;
      font-size: 22px;
      font-style: normal;
      font-weight: 450;
      line-height: normal;

      router-link {
        display: flex;
      }
    }
  }
}
</style>