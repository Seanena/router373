<script setup>
import { RouterLink } from 'vue-router'
import { ref } from 'vue';

const travellist = ref ([
 
  {name: 'One Cafe’',
  Facebook : 'One Cafe',
  GPS : "https://goo.gl/maps/GnVpBKhXBj6iSxsg7",
  img:"https://i.pinimg.com/originals/aa/62/61/aa62615fed8a48e115a43ddb065d3998.png"},

  {name: 'Two Cafe',
  Facebook : 'Two Cafe’',
  GPS : "https://goo.gl/maps/JmxHSYknfXJDdR3h6",
  img:"https://i.pinimg.com/originals/aa/62/61/aa62615fed8a48e115a43ddb065d3998.png"},

  {name: 'Three Cafe',
  Facebook : 'Three Cafe',
  GPS : "https://goo.gl/maps/K58wnHtHpvBDVfx97",
  img:"https://i.pinimg.com/originals/aa/62/61/aa62615fed8a48e115a43ddb065d3998.png"},

  {name: 'Four Cafe',
  Facebook : 'Four Cafe',
  GPS : "https://goo.gl/maps/PbJZvP68a2y8ow7SA",
  img:"https://i.pinimg.com/originals/aa/62/61/aa62615fed8a48e115a43ddb065d3998.png"},

  {name: 'Five Cafe',
  Facebook : 'Five Cafe',
  GPS : "https://goo.gl/maps/W3yi1Guh3CNw19YFA",
  img:"https://i.pinimg.com/originals/aa/62/61/aa62615fed8a48e115a43ddb065d3998.png"},

  {name: 'Six Cafe',
  Facebook : 'Six Cafe',
  GPS : "https://goo.gl/maps/irVioJsM6FB6E1u38",
  img:"https://i.pinimg.com/originals/aa/62/61/aa62615fed8a48e115a43ddb065d3998.png"},
]); 
</script>

<template>
    <div class="p-3 m-0 border-0 bd-example m-0 border-0">
      <div class="text-center">
        <div class="row row-cols-1 row-cols-md-3 g-4">
          <div class="col" v-for="(item, index) in travellist" :key="index">
            <div class="card text-bg-light h-100" style="width: 18rem">
              <img v-if="item.img" :src="item.img" class="card-img-top" alt="Place Image" />
              <div class="card-body">
                <h5 class="card-title">{{ item.name }}</h5>
                <RouterLink :to="{ name: 'ANewsCard', params: { name: item.name }}" class="icon-link gap-1 icon-link-hover stretched-link">
                  {{ item.name }}
                </RouterLink>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  