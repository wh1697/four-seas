<template>
  <view class="base">
    <!-- 轮播图区域大盒子 -->
    <view class="home">
      <!-- 轮播图区域 -->
      <swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000">
        <swiper-item>
          <view class="swiper-item">
            <image src="/static/icon/goods2.jpg" mode=""></image>
          </view>
        </swiper-item>
        <swiper-item>
          <view class="swiper-item">
            <image src="/static/icon/goods3.jpg" mode=""></image>
          </view>
        </swiper-item>
      </swiper>
    </view>

    <!-- 搜美食 -->
    <view class="search">
      <image src="/static/icon/3.png" mode=""></image>
      <input type="text" placeholder="搜美食,菜谱" class="comein">
    </view>
  </view>

  <!-- 轮播图下面的四个选项分类导航区域 -->
  <view class="nav-list">
    <navigator url="" v-for="(item,index) in list" :key="index">
      <image :src="item.pic" mode="" class="nav-img"></image>
      <text>{{item.text}}</text>
    </navigator>
  </view>

  <!-- 四海香婚庆 -->
  <view class="apply">
    <image src="/static/icon//8.png" mode=""></image>
  </view>

  <!-- 优选名厨 -->
  <view class="cooker">
    <image src="/static/icon/9.png" mode=""></image>
    <!-- 三个人物最大盒子 -->
    <view class="people">
      <!-- 第一个人 -->
      <view class="peoples">
        <image src="../../static/icon/man1.jpg" mode=""></image>
        <view class="uname">
          张小美
        </view>
      </view>
      <!-- 第二个人 -->
      <view class="peoples">
        <image src="../../static/icon/man2.jpg" mode=""></image>
        <view class="uname">
          王大牛
        </view>
      </view>
      <!-- 第三个人 -->
      <view class="peoples">
        <image src="../../static/icon/man3.jpg" mode=""></image>
        <view class="uname">
          斯塔克
        </view>
      </view>

    </view>
    <view class="more">
      更多名厨
    </view>
  </view>

  <!-- 优选餐宴 -->
  <view class="restaurant">
    <image src="/static/icon/10.png" mode=""></image>

    <!-- *****下面的轮播图****** -->
    <view class="love">
      <!-- 轮播图区域 -->
      <swiper :autoplay="true" :interval="3000" :duration="1000">
        <!-- 第一页 -->
        <swiper-item class="items">
          <navigator class="ab" url="">
            <image src="/static/icon/gg.jpg" mode=""></image>
            <!-- 下面商品名称+价格 -->
            <view class="zzz">
              <view class="">
                gvhbbh
              </view>
              <view class="">
                <text>￥4999/桌</text>
              </view>
            </view>
          </navigator>

          <navigator class="ab" url="">
            <image src="/static/icon/gg.jpg" mode=""></image>
            <!-- 下面商品名称+价格 -->
            <view class="zzz">
              <view class="">
                gvhbbh
              </view>
              <view class="">
                <text>￥4999/桌</text>
              </view>
            </view>
          </navigator>
        </swiper-item>

        <swiper-item class="items">
          <navigator class="ab" url="">
            <image src="/static/icon/gg.jpg" mode=""></image>
            <!-- 下面商品名称+价格 -->
            <view class="zzz">
              <view class="">
                gvhbbh
              </view>
              <view class="">
                <text>￥4999/桌</text>
              </view>
            </view>
          </navigator>

          <navigator class="ab" url="">
            <image src="/static/icon/gg.jpg" mode=""></image>
            <!-- 下面商品名称+价格 -->
            <view class="zzz">
              <view class="">
                gvhbbh
              </view>
              <view class="">
                <text>￥4999/桌</text>
              </view>
            </view>
          </navigator>
        </swiper-item>

      </swiper>
    </view>

    <view class="more-restaurant">
      更多餐宴
    </view>

  </view>


  <!-- 信用认证品质安全最大盒子 -->
  <view class="safe">

    <!-- 第一块 -->
    <view class="safe1">
      <!-- 左面图片 -->
      <image src="/static/icon/13.png" mode=""></image>
      <!-- 右面文字大盒子 -->
      <view class="word">
        <view class="">
          信用保障
        </view>
        <view class="">
          服务到位,时间准时
        </view>
      </view>
    </view>

    <!-- 第二块 -->
    <view class="safe1">
      <!-- 左面图片 -->
      <image src="/static/icon/13.png" mode=""></image>
      <!-- 右面文字大盒子 -->
      <view class="word">
        <view class="">
          信用保障
        </view>
        <view class="">
          服务到位,时间准时
        </view>
      </view>
    </view>

    <!-- 第三块 -->
    <view class="safe1">
      <!-- 左面图片 -->
      <image src="/static/icon/13.png" mode=""></image>
      <!-- 右面文字大盒子 -->
      <view class="word">
        <view class="">
          信用保障
        </view>
        <view class="">
          服务到位,时间准时
        </view>
      </view>
    </view>


    <!-- 第四块 -->
    <view class="safe1">
      <!-- 左面图片 -->
      <image src="/static/icon/13.png" mode=""></image>
      <!-- 右面文字大盒子 -->
      <view class="word">
        <view class="">
          信用保障
        </view>
        <view class="">
          服务到位,时间准时
        </view>
      </view>
    </view>

  </view>


  <!-- 首页最下面图片 -->
  <view class="bottom-pic">
    <image src="../../static/icon/gg.jpg" mode=""></image>
  </view>




</template>

<script>
  export default {
    data() {
      return {
        // 使用async 和  await 发请求 第三步 
        list: []
      };
    },
    methods: {
      // 使用async 和  await 发请求 第一步
      async getList() {
        let ret = await uni.request({
          url: 'http://api.brqc.com.cn/cpz/shxmp/navlist',
          data: {},
        })
        //因为接口这样子let ret = [null,data]我们要解构赋值或者取数组里面的第二个元素
        // let [err, res] = ret;    //解构赋值写法用数组解构
        console.log(ret);
        // 把数据放到data定义好的list里面
        // 使用async 和  await 发请求 第四步
        // this.list = ret[1].data.data //不用解构赋值的vue2写法取数组里面的第二个元素this.list = ret[1].data.data
        this.list = ret.data.data //不用解构赋值的vue2写法取数组里面的第二个元素this.list = ret.data.data

        // console.log(res.data.data);
        // this.list = res.data.data;   ////这样写也可以搭配解构赋值 let [err, res] = ret;

        // 需就是加一个动画数据正在加载中的效果 第二步
        uni.hideLoading(); //取到数据立即隐藏动画数据正在加载的效果

      }
    },
    onLoad() {
      // 使用async 和  await 发请求 第二步  // 在create(){}写也可以
      this.getList()
    },
  }
</script>

<style lang="scss">
  .base {
    position: relative;

    // 轮播图
    .home {
      background-color: #f5f5f5;

      swiper {
        height: 600rpx;



        .swiper-item,
        image {
          width: 100%;
          height: 100%;
        }



      }

      >>>.uni-swiper-wrapper {
        >>>.uni-swiper-dots-horizontal {
          position: absolute;
          bottom: 40rpx !important;
        }
      }

    }


    // 搜美食
    .search {
      // background-color: red;
      position: absolute;
      left: 50rpx;
      top: 550rpx;

      .comein {
        padding-left: 50%;
        box-sizing: border-box;
      }

      image {
        width: 50rpx;
        height: 50rpx;
        position: absolute;
        left: 111px;
        top: 10px;
      }

      input {
        width: 650rpx;
        height: 100rpx;
        background-color: #ffffff;
        margin: 0 auto;
        border-radius: 40rpx;
      }
    }

  }

  // 轮播图下面的四个选项分类导航区域
  .nav-list {
    display: flex;
    justify-content: space-between;
    width: 94%;
    background-color: pink;
    margin: 80rpx auto;

    navigator {
      display: flex;
      flex-direction: column;
      align-items: center;

      .nav-img {
        width: 120rpx;
        height: 120rpx;
      }
    }
  }

  // 四海香婚庆
  .apply {
    width: 94%;
    height: 400rpx;
    margin: 0 auto;

    image {
      width: 100%;
      height: 100%;
    }


  }

  // 优选名厨
  .cooker {
    width: 99%;
    height: 550rpx;
    background-color: pink;
    margin: 20rpx auto;

    image {
      width: 80%;
      height: 100rpx;
      margin: 0 auto;
      display: block;
    }

    .people {
      width: 90%;
      background-color: red;
      height: 350rpx;
      margin: 20rpx auto;
      display: flex;
      justify-content: space-around;

      .peoples {
        width: 30%;
        height: 300rpx;
        background-color: yellowgreen;

        image {
          width: 150rpx;
          height: 150rpx;
          border-radius: 50%;
          margin-top: 20rpx;
        }

        .uname {
          text-align: center;
        }
      }
    }

    .more {
      text-align: center;
      color: aliceblue;
    }
  }

  // 优选餐宴
  .restaurant {
    width: 99%;
    background-color: yellow;
    margin: 20rpx auto;

    image {
      width: 90%;
      height: 50rpx;
      display: block;
      margin: 0 auto;
    }

    .love {
      swiper {
        height: 400rpx;

        .items {
          // width: 400rpx;

          image {
            width: 300rpx;
            height: 200rpx;
            margin-left: 10rpx;
            // float: left;
            margin-top: 50rpx;
          }

          uni-navigator.ab {
            float: left;
            margin-left: 20rpx;
          }
        }
      }
    }

    .more-restaurant {
      text-align: center;
      font-size: 32rpx;
      color: #ffffff;
    }

  }

  // 信用认证品质安全最大盒子
  .safe {
    width: 100%;
    height: 500rpx;
    background-color: #ffffff;
    margin: 20rpx auto;

    .safe1 {
      width: 50%;
      height: 250rpx;
      // background-color: purple;
      float: left;

      image {
        width: 100rpx;
        height: 100rpx;
        float: left;
        margin-top: 60rpx;
        margin-left: 20rpx;
      }

      // 右面文字大盒子
      .word {
        float: left;
        // background-color: red;
        font-size: 28rpx;
        margin-top: 80rpx;
        margin-left: 10rpx;
      }
    }
  }
  
  .bottom-pic{
    width: 100%;
    height: 400rpx;
    background-color: blue;
    
    image{
      width: 100%;
      height: 100%;
    }
  }
</style>
