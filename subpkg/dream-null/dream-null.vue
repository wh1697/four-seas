<template>
  <view class="base">
    <!-- 头部左右标题+清空最大盒子 -->
    <view class="title">
      <!-- 收藏12个 -->
      <view class="collect">
        <image src="../../static/icon/icon_cha.png" mode=""></image>
        <text>已收藏0个餐宴</text>
      </view>
      <!-- 清空 -->
      <navigator url="../../subpkg/dream-null/dream-null">
        <view class="clear">
          <image src="../../static/icon/icon_clear.png" mode=""></image>
          <text>清空</text>
        </view>
      </navigator>

    </view>


    <view class="pic">
      <image src="../../static/icon/nomore2.png" mode=""></image>
    </view>
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

    .title {
      width: 100%;
      height: 100rpx;
      background-color: red;
      display: flex;
      justify-content: space-between;
      align-items: center;

      .collect {
        padding-left: 20rpx;
        display: flex;
        align-items: center;

        image {
          width: 50rpx;
          height: 50rpx;
        }

        text {
          padding-left: 20rpx;
        }
      }

      // 清空
      .clear {
        padding-right: 20rpx;
        display: flex;
        align-items: center;

        image {
          width: 40rpx;
          height: 40rpx;

        }
      }
    }

    // 中间图片
    .pic {
      width: 50%;
      // background-color: yellowgreen;
      margin: 350rpx auto;

      image {
        width: 300rpx;
        height: 300rpx;
        display: block;
        margin: 0 auto;
      }
    }
  }
</style>
