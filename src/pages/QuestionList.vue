<template>
  <q-page>
      <div v-if="$q.screen.lt.md"
      class="q-ma-sm">
      <img src="/smatur-logo.svg" />
    </div>
    <div class="textOne text-center q-pt-md text-uppercase">
      Poll result will be shown on 5th Feb 2024!
    </div>
    <div class="textTwo text-center q-py-sm">
      Which one is the most beautiful city in the world?
    </div>
    <div class="textThree text-center">
      Created by <span class="text-bold">Raheel Khan</span> on Jan 19, 2024 12:10 am
    </div>
    <div class="row justify-between">
    <div class="col-md-2 col-lg-2 col-xl-2 col-3" v-if="$q.screen.gt.sm"></div>
    <div class="q-mt-md col-grow">
      <q-item class="q-pa-none q-px-md q-gutter-x-md row justify-center">
        <q-card class="custom-btn q-pa-sm borderBtn container">
          <q-img
            src="image1.png"
            alt="Image"
            class="custom-image"
          />
          <div class="q-pt-sm">  <q-btn class="full-width btnElement" no-caps label="London"/></div>
        </q-card>
        <q-card class="custom-btn q-pa-sm borderBtn container">
          <q-img
            src="/image2.png"
            alt="Image"
            class="custom-image"
          />
         <div class="q-pt-sm">  <q-btn class="full-width btnElement" no-caps label="Sydney"/></div>
        </q-card>
      </q-item>
      <q-item class="q-pa-md q-gutter-x-md row justify-center">
         <q-card class="custom-btn q-pa-sm borderBtn container">
          <q-img
            src="/image3.png"
            alt="Image"
            class="custom-image"
          />
          <div class="q-pt-sm">  <q-btn class="full-width btnElement" no-caps label="New York"/>
          </div>
        </q-card>
        <q-card class="custom-btn q-pa-sm borderBtn container">
          <q-img
            src="/image4.png"
            alt="Image"
            class="custom-image"
          />
          <div class="q-pt-sm">  <q-btn class="full-width btnElement" no-caps label="Shanghai"/></div>
        </q-card>
      </q-item>
      </div>
      <div class="col-md-2 col-lg-2 col-xl-2 col-3 q-mt-xl q-pr-xl" v-if="$q.screen.gt.sm">
      <q-btn class="full-width text-color" style="background: #42307D1A;" label="Invite Friends" no-caps />
      <q-card class="">
      <q-card-section class="q-mt-md">
      <div class="text-grey-7 q-pb-xs text-caption">Share</div>
      <div class="text-caption q-py-xs row" v-for="item in itemList" :key="item.color">
      <div class="q-mr-sm">
     <q-item-label> <img :src='item.image'/></q-item-label>
      </div>
      <div class="q-mt-xs"><q-item-label :style="{color: item.color}">{{ item.title }}</q-item-label></div>
      </div>
      </q-card-section>
      </q-card>
       <div class="q-my-sm text-center">
      <span class="q-mt-md q-mr-sm "><img src="flag.png"/></span><span class="text-grey-7 text-caption">Report Abuse</span>
      </div>
      </div>
      </div>
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      itemList: [
        {
          color: "#00AAEC",
          image: 'twitter.png',
          title: "Share on twitter",
        },
        {
          color: "#4460A0",
          image: 'facebook.png',
          title: "Share on facebook",
        },
        {
          color: "#00D856",
          image: 'whatsapp.png',
          title: "Share on whatsapp",
        },
        {
          color: "#FF9E72",
          image: 'share.png',
          title: "Share link",
        },
        {
          avatar: "#A46CFF",
          image: 'qrcode.png',
          title: "Share QR code",
        },
      ],
    };
  },
};
</script>
<style>
.textOne {
  font-size: .95rem;
  font-weight: 600;
  text-align: center;
  color: #42307d;
}
.textTwo {
  font-size: 1.6rem;
  font-weight: 600;
  text-align: center;
}
.textThree {
  font-size: .8rem;
  font-weight: 500;
  text-align: center;
  color: #b1b1b1;
}
.btnElement{
background: #42307D;;
}
.custom-btn {
  max-width: 340px;
  width: 50%;
  background-color: #ffff;
}
.container {
  text-align: center;
  color: white;
  
}

.lebel-margin {
  font-weight: 400;
}
</style>
