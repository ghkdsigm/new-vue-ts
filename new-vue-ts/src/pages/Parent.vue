<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <child parentMessage="안녕"></child>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
import Child from '@/components/prop/Child.vue';

@Component({
    components: {
        Child,
    },
})

export default class Home extends Vue {}
</script>