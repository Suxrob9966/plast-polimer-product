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
          <q-img :src="group.img" :ratio="1" style="width:250px">
            <div class="absolute-bottom text-subtitle2 text-center">
              {{ group.title }}
            </div>
          </q-img>
        </q-card>
      </div>
    </div>

    <div class="row full-width q-py-md">
      <div class="col-xs-12 col-sm-12 col-md-4"></div>
      <div class="col-xs-12 col-sm-12 col-md-8 bg-indigo-9 text-left text-h3 text-bold text-white q-pa-md headlines">
        &nbsp;Products
      </div>
    </div>

    <div class="row q-pt-md">
      <div class="col-xs-12">
        <div class="row text-h5 product" ref="description" id="description">
          <div class="col-xs-1 text-center">
            <q-img src="product/a5.png" style="width:55px; height: auto;"></q-img>
          </div>
          <div class="col-xs-11 q-pl-lg">
            <span class="text-bold">Polybags T-shirt.</span> They are used for free budget packaging and delivery of
            purchases at the checkout, temporary storage and transportation. Different sizes, material thickness, color
            and design - with and without a pattern - allow you to make a choice taking into account the assortment of
            the outlet and the possible load.
          </div>
        </div>
      </div>
    </div>

    <div class="row q-pt-lg">
      <div class="col-xs-12">
        <div class="row text-h5 product" ref="description1" id="description1">
          <div class="col-xs-1 text-center">
            <q-img src="product/ke.png" style="width:50px; height: auto;"></q-img>
          </div>
          <div class="col-xs-11 q-pl-lg">
            <span class="text-bold ">Стакан с картонной этикеткой – комбинация пластика и картона.</span> На наружную
            поверхность
            изготовленного полипропиленового стакана наклеивается картонная этикетка.
          </div>
        </div>
      </div>
    </div>

    <div class="row q-pt-lg">
      <div class="col-xs-12">
        <div class="row text-h5 product" ref="description2" id="description2">
          <div class="col-xs-1 text-center">
            <q-img src="product/my.png" style="width:50px; height: auto;"></q-img>
          </div>
          <div class="col-xs-11 q-pl-lg">
            <span class="text-bold ">Стакан с термоусадочной этикеткой.</span> На наружную поверхность полипропиленового
            стакана усаживается термоусадочная этикетка. Печать наносится на внутреннюю поверхность этикетки, благодаря
            чему изображение долго сохраняет свою насыщенность и не истирается.
          </div>
        </div>
      </div>
    </div>

    <div class="row q-pt-lg">
      <div class="col-xs-12">
        <div class="row text-h5 product" ref="description3" id="description3">
          <div class="col-xs-1 text-center">
            <q-img src="product/a8.png" style="width:50px; height: auto;"></q-img>
          </div>
          <div class="col-xs-11 q-pl-lg">
            <span class="text-bold ">Крышки на стаканы.</span> Мы производим полипропиленовые крышки «нахлобучки»
            (поверх крышки для фольги) высокого качества, пригодные для надевания на стакан на высокоскоростных
            разливочных линиях.
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script setup>
import { defineComponent } from 'vue'

const groups = [
  { img: "product/bag_blue.png", title: "Bags", ref: "description" },
  { img: "product/box.png", title: "Box", ref: "description1" },
  { img: "product/bucket_blue.png", title: "Bucket", ref: "description2" },
  { img: "product/bucket_yellow.png", title: "Big bucket", ref: "description3" },
  { img: "product/hot_water_pipe.png", title: "Water pipe", ref: "description4" },
  { img: "product/sand_toys.png", title: "Sand toys", ref: "description5" },
  { img: "product/truck_sm.png", title: "Truck toy", ref: "description6" },
]

</script>
<style lang="sass" scoped>
.top-img
  background: url(/tools/1.jpg)
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

</style>