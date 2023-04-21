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
    <navigator url="">
      <image src="/static/icon/6.png" mode="" class="nav-img"></image>
      <image src="/static/icon/7.png" mode="" class="nav-img"></image>
      <image src="/static/icon/8.png" mode="" class="nav-img"></image>
      <text></text>
    </navigator>
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
          url: 'http://api.brqc.com.cn/cpz/list.php',
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
      top: 590rpx;

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
    width: 700rpx;
    margin: 20rpx auto;
    border-radius: 15rpx;
    // background: #ffffff;
    background-color: pink;
    padding: 15rpx;

    display: flex;
    justify-content: space-between;

    .nav-img {
      width: 93rpx;
      height: 87rpx;
      margin: 0 auto;
    }

    navigator {
      display: flex;
      flex-direction: column;
    }
  }
</style>
