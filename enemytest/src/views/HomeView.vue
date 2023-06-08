<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src
import EnemyRepository from '@logic/enemy-repository'

@Options({
  components: {
    HelloWorld,
  },
  methods: {
    init() {
      EnemyRepository.getEnemy("1");
    }
  }
})
export default class HomeView extends Vue {}
</script>
