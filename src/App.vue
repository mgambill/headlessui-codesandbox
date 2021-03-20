<template>
  <section class="justify-center flex-1">
    <div class="container pt-8 mx-auto">
      <header class="grid grid-cols-3 w-full">
        <router-link custom to="/listbox" v-slot="{ navigate, isActive }">
          <button :class="`${ isActive ? 'bg-gray-100' : 'bg-indigo-100'} p-2`" @click="navigate">Listbox</button>
        </router-link>
        <router-link custom to="/menu" v-slot="{ navigate, isActive }">
          <button @click="navigate">Menu</button>  {{ isActive }}
        </router-link>
        <router-link custom to="/switch" v-slot="{ navigate, isActive }">
          <button @click="navigate">Switch</button> {{ isActive }}
        </router-link>
      </header>
       
      <router-view></router-view>
    </div>
  </section>  
</template>

<script lang="ts">
import HelloWorld from './components/HelloWorld.vue'
export default {
  components: {
    HelloWorld,
  },
}
</script>
