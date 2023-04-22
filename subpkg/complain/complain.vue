<template>
  <view class="base">
    <view class="complain">
      <!-- 标题 -->
      <text class="type">投诉类型</text>

      <!-- 三个选项 -->
      <view class="choose">
        <view class="serve">
          服务态度
        </view>

      </view>
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

    .complain {
      width: 100%;
      height: 200rpx;
      background-color: red;
      padding: 30rpx 0 0 30rpx;
      box-sizing: border-box;

      // 标题 
      .type {
        font-size: 40rpx;
        font-weight: 600;
      }
    }

  }
</style>
