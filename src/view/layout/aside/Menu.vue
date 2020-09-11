<template>
  <ul class="menu-nav">
    <router-link to="/" v-slot="{ href, navigate, isActive, isExactActive }">
      <li
        aria-haspopup="true"
        data-menu-toggle="hover"
        class="menu-item"
        :class="[
          isActive && 'menu-item-active',
          isExactActive && 'menu-item-active'
        ]"
      >
        <a :href="href" class="menu-link" @click="navigate">
          <i class="menu-icon flaticon2-architecture-and-city"></i>
          <span class="menu-text">About R&D Portal</span>
        </a>
      </li>
    </router-link>
    <router-link to="/" v-slot="{ href, navigate, isActive, isExactActive }">
      <li
        aria-haspopup="true"
        data-menu-toggle="hover"
        class="menu-item"
        :class="[
          isActive && 'menu-item-active',
          isExactActive && 'menu-item-active'
        ]"
      >
        <a :href="href" class="menu-link" @click="navigate">
          <i class="menu-icon flaticon2-architecture-and-city"></i>
          <span class="menu-text">Tutorial</span>
        </a>
      </li>
    </router-link>

    <li class="menu-section">
      <h4 class="menu-text">Data Sets</h4>
      <i class="menu-icon flaticon-more-v2"></i>
    </li>
    <router-link
      to="/data/upload"
      v-slot="{ href, navigate, isActive, isExactActive }"
    >
      <li
        aria-haspopup="true"
        data-menu-toggle="hover"
        class="menu-item"
        :class="[
          isActive && 'menu-item-active',
          isExactActive && 'menu-item-active'
        ]"
      >
        <a :href="href" class="menu-link" @click="navigate">
          <i class="menu-icon flaticon-upload"></i>
          <span class="menu-text">Data Upload</span>
        </a>
      </li>
    </router-link>
    <router-link to="/" v-slot="{ href, navigate, isActive, isExactActive }">
      <li
        aria-haspopup="true"
        data-menu-toggle="hover"
        class="menu-item"
        :class="[
          isActive && 'menu-item-active',
          isExactActive && 'menu-item-active'
        ]"
      >
        <a :href="href" class="menu-link" @click="navigate">
          <i class="menu-icon flaticon-file-2"></i>
          <span class="menu-text">Data Mgmt</span>
        </a>
      </li>
    </router-link>

    <!-- Model -->
    <li class="menu-section">
      <h4 class="menu-text">Model</h4>
      <i class="menu-icon flaticon-more-v2"></i>
    </li>

    <router-link
      to="/model"
      v-slot="{ href, navigate, isActive, isExactActive }"
    >
      <li
        aria-haspopup="true"
        data-menu-toggle="hover"
        class="menu-item"
        :class="[
          isActive && 'menu-item-active',
          isExactActive && 'menu-item-active'
        ]"
      >
        <a :href="href" class="menu-link" @click="navigate">
          <i class="menu-icon flaticon-interface-4"></i>
          <span class="menu-text">Model 학습</span>
        </a>
      </li>
    </router-link>

    <router-link
      to="/model"
      v-slot="{ href, navigate, isActive, isExactActive }"
    >
      <li
        aria-haspopup="true"
        data-menu-toggle="hover"
        class="menu-item"
        :class="[
          isActive && 'menu-item-active',
          isExactActive && 'menu-item-active'
        ]"
      >
        <a :href="href" class="menu-link" @click="navigate">
          <i class="menu-icon flaticon-interface-4"></i>
          <span class="menu-text">Model 관리</span>
        </a>
      </li>
    </router-link>

    <router-link
      to="/model"
      v-slot="{ href, navigate, isActive, isExactActive }"
    >
      <li
        aria-haspopup="true"
        data-menu-toggle="hover"
        class="menu-item"
        :class="[
          isActive && 'menu-item-active',
          isExactActive && 'menu-item-active'
        ]"
      >
        <a :href="href" class="menu-link" @click="navigate">
          <i class="menu-icon flaticon-interface-4"></i>
          <span class="menu-text">시뮬레이션</span>
        </a>
      </li>
    </router-link>

    <!-- Project 관리 -->
    <li class="menu-section">
      <h4 class="menu-text">Project 관리</h4>
      <i class="menu-icon flaticon-more-v2"></i>
    </li>

    <router-link
      to="/project"
      v-slot="{ href, navigate, isActive, isExactActive }"
    >
      <li
        aria-haspopup="true"
        data-menu-toggle="hover"
        class="menu-item"
        :class="[
          isActive && 'menu-item-active',
          isExactActive && 'menu-item-active'
        ]"
      >
        <a :href="href" class="menu-link" @click="navigate">
          <i class="menu-icon flaticon-interface-3"></i>
          <span class="menu-text">연구노트 관리</span>
        </a>
      </li>
    </router-link>

    <!-- Private 관리 -->
    <li class="menu-section">
      <h4 class="menu-text">Private Portal 관리</h4>
      <i class="menu-icon flaticon-more-v2"></i>
    </li>

    <router-link
      to="/private"
      v-slot="{ href, navigate, isActive, isExactActive }"
    >
      <li
        aria-haspopup="true"
        data-menu-toggle="hover"
        class="menu-item"
        :class="[
          isActive && 'menu-item-active',
          isExactActive && 'menu-item-active'
        ]"
      >
        <a :href="href" class="menu-link" @click="navigate">
          <i class="menu-icon flaticon2-architecture-and-city"></i>
          <span class="menu-text">맴버 관리</span>
        </a>
      </li>
    </router-link>
    <router-link
      to="/project/1"
      v-slot="{ href, navigate, isActive, isExactActive }"
    >
      <li
        aria-haspopup="true"
        data-menu-toggle="hover"
        class="menu-item"
        :class="[
          isActive && 'menu-item-active',
          isExactActive && 'menu-item-active'
        ]"
      >
        <a :href="href" class="menu-link" @click="navigate">
          <i class="menu-icon flaticon-interface-4"></i>
          <span class="menu-text">프로젝트 관리</span>
        </a>
      </li>
    </router-link>
  </ul>
</template>

<script>
export default {
  name: "KTMenu",
  methods: {
    hasActiveChildren(match) {
      return this.$route["path"].indexOf(match) !== -1;
    }
  }
};
</script>
