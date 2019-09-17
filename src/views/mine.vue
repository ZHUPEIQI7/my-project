<template>
  <div class="loadContent">
    <div class="card" v-for="(item) in list" :key="item.name" >

      <div class="origin-model">
        <img :src="item.img" alt />
      </div>

      <div class="model">
        <img :src="item.loadImg" alt />
      </div>

    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class Home extends Vue {
  public list: Array<any> = [
    {
      name: "智信Android版",
      img: require("@/assets/android.png"),
      showModel: false,
      loadImg: require("@/assets/load.png"),
    },
    {
      name: "智信iPhone版",
      img: require("@/assets/apple.png"),
      showModel: false,
      info: "",
      loadImg: require("@/assets/load.png"),     
    },
    {
      name: "智信Mac版",
      img: require("@/assets/mac.png"),
      showModel: false,
      info: "点击下载智信Mac版",
      loadImg: require("@/assets/load.png"), 
    },
    {
      name: "智信Windows版",
      img: require("@/assets/windows.png"),
      showModel: false,
      info: "点击下载智信windows版",
      loadImg: require("@/assets/load.png"),
    }
  ];

//   private hoverCard(item: any, idx: number) {
//     this.list[idx].showModel = true;
//     alert(this.list[name])
//   }

//   private outCard(item: any, idx: number) {
//     this.list[idx].showModel = false;
//   }
}
  </script>

  <style lang="scss" scoped>
    .loadContent {
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      justify-content:center;

      .card:hover .model{
        display: block;
      }
      .card:hover .origin-model{
        display: none;
      }

      .card {
        width: 168px;
        height: 168px;
        text-align: center;
        display: block;
        position: relative;
        cursor: pointer;
        color: #999;
        margin-right: 10px;
        box-sizing: border-box;
        font-size: 14px;
        font-family: Microsoft YaHei;
        font-weight: 400;
        background: rgb(250, 250, 250);
        border: 1px solid rgb(30, 179, 141);
        border-radius: 2px;

        .origin-model{
          padding-top: 30px;
          img {         
            width: 60px;
            height: 60px;
            margin-bottom: 20px;
          }
        }
                      
        .model {
          display: none;
          padding-top: 30px;
          img {
              width: 60px;
              height: 60px;
              margin-bottom: 20px;
          }
        }
      }  
    }
    
  
  </style>