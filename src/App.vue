<script setup>
import Header from './Header.vue';
import About from './About.vue';
import Brand from './Brand.vue';
import Feature from './Feature.vue';
import Active from './Active.vue';
import Menu from './Menu.vue';
import Profiles from './Profiles.vue';
import information from './information.vue';
import Foot from './Foot.vue';
import goTo from './goTo.vue';
</script>

<template>
<Header></Header>
<About></About>
<Brand></Brand>
<Feature></Feature>
<Active></Active>
<Menu></Menu>
<Profiles></Profiles>
<information></information>
<Foot></Foot>
<goTo></goTo>
</template>

<style>
body{
  margin: 0;
  padding: 0;
}
body::-webkit-scrollbar {
  display: none;
}
</style>
