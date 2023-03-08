<template>
  <q-page class="flex flex-center" style="background: #f5f7f5;">
    <!-- title -->
    <div class="full-width top-img header gt-xs">
      <div class="title text-left text-h3 text-bold title-top q-pt-xl q-pl-xl">
        <!-- <q-img src="/logo.svg" style="width: 15vmax; height: auto" class="logo" /> -->
      </div>
      <div class="title text-center text-h4 text-bold title-bottom full-width q-pa-md">
        <span class="full-width">
          Plast Polimer Product
        </span>
      </div>
    </div>

    <!-- products -->
    <div class="row text-h6 text-center full-width q-ma-lg gt-xs">
      <div class="fit row wrap justify-center content-center q-gutter-xl">
        <q-card class="my-card" v-for="group in groups" :key="group.img" @click="scrollToText(group.ref)">
          <q-img :src="group.img" :ratio="4 / 3" style="width:250px">
            <div class="absolute-bottom text-subtitle2 text-center">
              {{ group.title }}
            </div>
          </q-img>
        </q-card>
      </div>
    </div>

    <!-- <div class="row full-width q-py-md">
      <div class="col-xs-12 col-sm-12 col-md-4"></div>
      <div class="col-xs-12 col-sm-12 col-md-8 bg-indigo-9 text-left text-h3 text-bold text-white q-pa-md headlines">
        &nbsp;Products
      </div>
    </div> -->

    <div class="row q-py-md">
      <span class="text-center text-h3 bg-indigo-9 text-bold text-white q-pa-lg tabs ">Products</span>
    </div>

    <div class="row q-pt-md">
      <div class="col-xs-12">
        <div class="row text-h5 product" ref="description" id="description">
          <div class="col-xs-1 text-center">
            <q-img src="product/bag_blue.png" style="width:55px; height: auto;"></q-img>
          </div>
          <div class="col-xs-11 q-pl-lg">
            <span class="text-bold">Polybags T-shirt.</span> They are used for free budget packaging and delivery of
            purchases at the checkout, temporary storage and transportation.
          </div>
        </div>
      </div>
    </div>

    <div class="row q-pt-lg">
      <div class="col-xs-12">
        <div class="row text-h5 product" ref="description1" id="description1">
          <div class="col-xs-1 text-center">
            <q-img src="product/box.png" style="width:50px; height: auto;"></q-img>
          </div>
          <div class="col-xs-11 q-pl-lg">
            <span class="text-bold ">Polybox for vegetables and fruits. </span>Practicality during transportation,
            ease of storage of products, easy cleaning - these are the necessary qualities for boxes. Our boxes are made
            of environmentally friendly material, have a long service life.
          </div>
        </div>
      </div>
    </div>

    <div class="row q-pt-lg">
      <div class="col-xs-12">
        <div class="row text-h5 product" ref="description2" id="description2">
          <div class="col-xs-1 text-center">
            <q-img src="product/bucket_blue.png" style="width:50px; height: auto;"></q-img>
          </div>
          <div class="col-xs-11 q-pl-lg">
            <span class="text-bold ">Polypropylene bucket.</span> A plastic bucket is useful at home, in
            the country house, in construction and during repairs. It is light, easy to clean and does not corrode,
            unlike a
            metal bucket.
          </div>
        </div>
      </div>
    </div>

    <div class="row q-pt-lg">
      <div class="col-xs-12">
        <div class="row text-h5 product" ref="description3" id="description3">
          <div class="col-xs-1 text-center">
            <q-img src="product/bucket_yellow.png" style="width:50px; height: auto;"></q-img>
          </div>
          <div class="col-xs-11 q-pl-lg">
            <span class="text-bold ">Polypropylene basin.</span> It is designed for any household purposes:
            suitable for fine hand washing, washing dishes, vegetables and fruits, cleaning the house. The basin is
            equipped with two handles, thanks to which it is convenient to rearrange it from place to place.
          </div>
        </div>
      </div>
    </div>

    <div class="row q-pt-lg">
      <div class="col-xs-12">
        <div class="row text-h5 product" ref="description4" id="description4">
          <div class="col-xs-1 text-center">
            <q-img src="product/hot_water_pipe.png" style="width:50px; height: auto;"></q-img>
          </div>
          <div class="col-xs-11 q-pl-lg">
            <span class="text-bold ">Polypropylene pipes.</span> These pipes are used in systems such as cold, hot water
            supply and heating in various residential and industrial facilities and buildings, can be used in the laying
            of technical pipelines, in ventilation systems, as well as in agriculture.
          </div>
        </div>
      </div>
    </div>

    <div class="row q-pt-lg">
      <div class="col-xs-12">
        <div class="row text-h5 product" ref="description5" id="description5">
          <div class="col-xs-1 text-center">
            <q-img src="product/sand_toys_1.png" style="width:50px; height: auto;"></q-img>
          </div>
          <div class="col-xs-11 q-pl-lg">
            <span class="text-bold ">Sand toys.</span> These toys bring the fun of the beach to your own back
            garden. From a truck tool set to a bucket and spade set, we have everything that your little one will need
            for the seaside experience.
          </div>
        </div>
      </div>
    </div>

    <div class="row q-pt-lg">
      <div class="col-xs-12">
        <div class="row text-h5 product" ref="description6" id="description6">
          <div class="col-xs-1 text-center">
            <q-img src="product/truck_sm.png" style="width:50px; height: auto;"></q-img>
          </div>
          <div class="col-xs-11 q-pl-lg">
            <span class="text-bold ">Truck toys.</span> A plastic toy truck with a body is sure to please the child, it
            will help develop imagination and fine motor skills. The child will be able to carry various loads, small
            toys and much more in the back of his truck.
          </div>
        </div>
      </div>
    </div>

    <br>
    <br>

    <!-- description -->
    <div class="row">
      <div class="col-sm-6 col-xs-12">
        <div class="text-left text-h4 text-bold q-ma-lg q-pl-xl ">
          About us
        </div>
        <div class="row q-ma-lg q-pl-xl text-h5">
          Our company is widely represented in such segments of the polymer market as high and low pressure
          polyethylene, linear polyethylene, polypropylene.
        </div>
      </div>
      <div class="col-sm-6 col-xs-12">
        <div class="row q-pl-xl q-pt-lg text-h5">
          <ul>
            <li>150 tonns of polyethylene</li>
            <li>500 tonns of polypropylene</li>
          </ul>
        </div>
      </div>
    </div>


  </q-page>
</template>

<script setup>
import { defineComponent, ref } from "vue";
import { scroll } from 'quasar';
const { getScrollTarget, setVerticalScrollPosition } = scroll;

const groups = [
  { img: "product/bag_blue.png", title: "Bags", ref: "description" },
  { img: "product/box.png", title: "Box", ref: "description1" },
  { img: "product/my.png", title: "Bucket", ref: "description2" },
  { img: "product/bucket_yellow.png", title: "Basin", ref: "description3" },
  { img: "product/hot_water_pipe.png", title: "Water pipe", ref: "description4" },
  { img: "product/sand_toys_1.png", title: "Sand toys", ref: "description5" },
  { img: "product/truck_sm.png", title: "Truck toy", ref: "description6" },
]

const ordering = ref(null);
const scrollTo = () => {
  const el = ordering.value
  const target = getScrollTarget(el)
  const offset = el.offsetTop
  const duration = 300
  setVerticalScrollPosition(target, offset, duration)
}

const description = ref(null);
const description1 = ref(null);
const description2 = ref(null);
const description3 = ref(null);
const description4 = ref(null);
const description5 = ref(null);
const description6 = ref(null);
let el;
let target;
let offset;
let duration;
const scrollToText = (data) => {
  if (data === description.value.id) {
    el = description.value;
  }
  else if (data === description1.value.id) {
    el = description1.value;
  }
  else if (data === description2.value.id) {
    el = description2.value;
  }
  else if (data === description3.value.id) {
    el = description3.value;
  }
  else if (data === description4.value.id) {
    el = description4.value;
  }
  else if (data === description5.value.id) {
    el = description5.value;
  }
  else {
    el = description6.value;
  }
  target = getScrollTarget(el);
  offset = el.offsetTop;
  duration = 300;
  setVerticalScrollPosition(target, offset, duration);
}

</script>
<style lang="sass" scoped>
.top-img
  background: url(/tools/1.png)
  background-size: cover
  background-position: center
  background-attachment: fixed
  background-repeat: no-repeat

.header
  position: relative
  min-height: 550px

.title
  color: #f5f7f5
  text-shadow: 1px 1px #000000

.title-bottom
  position: absolute
  top: 250px
  background-image: linear-gradient(rgba(0,0,0,0), rgba(0,0,0,1))
  height: 300px
  display: flex

.title-top
  background-image: linear-gradient(rgba(0,0,0,1), rgba(0,0,0,0))
  height: 90px
  
.title-bottom span, .title-bottom-sm span
  align-self: flex-end


.tabs
  border-radius: 15px
</style>