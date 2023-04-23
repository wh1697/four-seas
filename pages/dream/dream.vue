<template>
  <view class="base">
    <!-- 头部左右标题+清空最大盒子 -->
    <view class="title">
      <!-- 收藏12个 -->
      <view class="collect">
        <image src="../../static/icon/icon_cha.png" mode=""></image>
        <text>已收藏12个餐宴</text>
      </view>
      <!-- 清空 -->
      <navigator url="../../subpkg/dream-null/dream-null">
        <view class="clear">
          <image src="../../static/icon/icon_clear.png" mode=""></image>
          <text>清空</text>
        </view>
      </navigator>

    </view>


    <!-- 图片+商品名称价格收藏最大盒子   第一个 -->
    <view class="shop">
      <!-- 商品图片 -->
      <image src="../../static/icon/goods3.jpg" mode=""></image>
      <!-- 热度 -->
      <view class="hot">
        <image src="../../static/icon/icon_fire.png" mode=""></image>
        18888
      </view>
      <!-- 商品名称价格收藏最大盒子 -->
      <view class="price">

        <!-- 商品名称价格盒子 -->
        <view class="uname">
          <view class="">
            盛夏海鲜家宴
          </view>
          <view class="">
            ￥4999/桌
          </view>
        </view>

        <!-- 收藏盒子 -->
        <view class="collets">
          <view class="">
            <image src="../../static/icon/92.png" mode=""></image>
          </view>
          <view class="">
            取消收藏
          </view>
        </view>

      </view>
    </view>


    <!-- 图片+商品名称价格收藏最大盒子   第二个 -->
    <view class="shop">
      <!-- 商品图片 -->
      <image src="../../static/icon/goods3.jpg" mode=""></image>
      <!-- 热度 -->
      <view class="hot">
        <image src="../../static/icon/icon_fire.png" mode=""></image>
        18888
      </view>
      <!-- 商品名称价格收藏最大盒子 -->
      <view class="price">

        <!-- 商品名称价格盒子 -->
        <view class="uname">
          <view class="">
            盛夏海鲜家宴
          </view>
          <view class="">
            ￥4999/桌
          </view>
        </view>

        <!-- 收藏盒子 -->
        <view class="collets">
          <view class="">
            <image src="../../static/icon/92.png" mode=""></image>
          </view>
          <view class="">
            取消收藏
          </view>
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

    .title {
      width: 100%;
      height: 100rpx;
      // background-color: red;
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

    .shop {
      width: 94%;
      height: 700rpx;
      margin: 20rpx auto;
      // background-color: pink;
      position: relative;

      image {
        width: 100%;
        height: 500rpx;
      }

      .hot {
        width: 200rpx;
        height: 70rpx;
        position: absolute;
        left: 500rpx;
        top: 418rpx;
        background-color: gray;
        border-radius: 20rpx;

        image {
          width: 50rpx;
          height: 50rpx;
          margin-left: 20rpx;

        }
      }

      .price {
        width: 100%;
        // background-color: aqua;
        height: 180rpx;
        display: flex;
        justify-content: space-between;

        .uname {
          padding-left: 30rpx;
          margin-top: 50rpx;
        }

        .collets {
          padding-right: 20rpx;
          margin-top: 50rpx;

          image {
            width: 50rpx;
            height: 50rpx;
            margin-left: 40rpx;
          }
        }
      }


    }
  }
</style>
