<template>
  <view class="base">
    <!-- 标题+头像大盒子 -->
    <view class="content">
      <!-- 左侧标题 -->
      <view class="title">
        <view class="sky">
          天下第壹吃货
        </view>
        <view class="comein">
          欢迎您光临四海香!
        </view>
      </view>
      <!-- 右侧头像 -->
      <image src="/static/icon/man1.jpg" mode=""></image>
    </view>

    <!-- 烹饪历史 -->
    <navigator url="../../subpkg/edge/edge">
      <view class="history">
        <!-- 左侧 -->
        <view class="historys">
          <image src="/static/icon/icon_order.png" mode=""></image>
          <text>烹饪历史</text>
        </view>

        <!-- 右侧 -->
        <view class="arrow">
          》
        </view>
      </view>
    </navigator>


    <!-- 支付记录 -->
    <view class="history">
      <!-- 左侧 -->
      <view class="historys">
        <image src="/static/icon/icon_money.png" mode=""></image>
        <text>支付记录</text>
      </view>

      <!-- 右侧 -->
      <view class="arrow">
        》
      </view>
    </view>


    <!-- 举报投诉 -->
    <navigator url="../../subpkg/complain/complain">
      <view class="history">
        <!-- 左侧 -->
        <view class="historys">
          <image src="/static/icon/icon_msg.png" mode=""></image>
          <text>举报投诉</text>
        </view>

        <!-- 右侧 -->
        <view class="arrow">
          》
        </view>
      </view>
    </navigator>



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

    .content {
      width: 100%;
      height: 200rpx;
      // background-color: red;
      display: flex;
      justify-content: space-between;

      .title {
        padding-left: 40rpx;
        line-height: 70rpx;
        margin-top: 20rpx;

        .sky {
          font-size: 50rpx;
          font-weight: 600;
        }

        .comein {
          font-size: 30rpx;
          color: gray;
        }
      }

      image {
        width: 120rpx;
        height: 120rpx;
        border-radius: 50%;
        margin-right: 40rpx;
        margin-top: 50rpx;
      }

    }

    // 烹饪历史
    .history {
      width: 99%;
      height: 100rpx;
      // background-color: yellowgreen;
      border-bottom: 1px solid black;
      display: flex;
      justify-content: space-between;
      align-items: center;


      // 左侧
      .historys {
        padding-left: 20rpx;
        display: flex;
        align-items: center;

        image {
          width: 50rpx;
          height: 50rpx;
        }

        text {
          padding-left: 30rpx;
        }

      }

      // 右侧
      .arrow {}


    }
  }
</style>
