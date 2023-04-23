<template>
  <view class="base">
    <view class="complain">
      <!-- 标题 -->
      <text class="type">投诉类型</text>

      <!-- 三个选项大盒子 -->
      <view class="choose">
        <view class="serve">
          服务态度
        </view>
        <view class="serve">
          服务态度
        </view>
        <view class="serve">
          服务态度
        </view>

      </view>
    </view>


    <!-- 投诉详细说明 -->
    <view class="tell">
      <textarea name="" id="" cols="30" rows="10" placeholder="输入投诉详细说明(选填)"></textarea>
    </view>

    <!-- 图片上传 -->
    <view class="pic">
      <image src="/static/icon/goods2.jpg" mode=""></image>
    </view>

    <!-- 底部按钮 -->
    <button>提交</button>
  </view>
</template>

<script>
  export default {
    data() {
      return {

      };
    }
  }
</script>

<style lang="scss">
  .base {
    background-color: #f5f5f5;

    .complain {
      width: 100%;
      height: 200rpx;
      // background-color: pink;
      padding: 30rpx 0 0 30rpx;
      box-sizing: border-box;
      box-shadow: #ffffff;

      // 标题 
      .type {
        font-size: 40rpx;
        font-weight: 600;
      }

      // 三个选项大盒子
      .choose {
        width: 100%;
        height: 100rpx;
        // background-color: brown;
        display: flex;
        justify-content: flex-start;
        margin-top: 10rpx;

        .serve {
          width: 200rpx;
          height: 80rpx;
          background-color: red;
          border-radius: 50rpx;
          text-align: center;
          line-height: 80rpx;
          color: #ffffff;
          margin-left: 10rpx;
        }
      }

    }

    // 投诉详细说明
    .tell {
      width: 100%;
      height: 400rpx;
      // background-color: aquamarine;
      margin: 10rpx auto;

      textarea {
        padding-left: 30rpx;
      }
    }

    // 图片上传
    .pic {
      width: 100%;
      height: 500rpx;
      // background-color: blueviolet;
     // background-color: rgb(255, 255, 255);

      image {
        width: 200rpx;
        height: 200rpx;
        margin-top: 30rpx;
        margin-left: 30rpx;
      }
    }


    // 提交按钮
    button {
      background-color: orangered;
    }

  }
</style>
