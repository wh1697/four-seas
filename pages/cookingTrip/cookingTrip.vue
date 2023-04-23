<template>
  <view class="base">
    <!-- 头部左右标题+历史最大盒子 -->
    <view class="title">
      <!-- 收藏12个 -->
      <view class="collect">
        <image src="../../static/icon/icon_cha.png" mode=""></image>
        <text>已有9个行程</text>
      </view>
      <!-- 历史 -->
      <view class="clear">
        <image src="/static/icon/92.png" mode=""></image>
        <text>历史</text>
      </view>
    </view>


    <!-- 图片+商品名称价格收藏最大盒子   第一个 -->
    <view class="shop">
      <!-- 图片上面的两条信息 -->
      <view class="info">
        <!-- 第一条信息 -->
        <view class="infos">
          <image src="../../static/icon/77.png" mode=""></image>
          <text>05-09 11:40 周三 名厨上门</text>
        </view>
        <!-- 第二条信息 -->
        <view class="infos">
          <image src="/static/icon/91.png" mode=""></image>
          <text>涪城区长虹国际大道翡翠绿湾1栋2单元1802</text>
        </view>
      </view>
      <!-- 商品图片 -->
      <image src="../../static/icon/goods3.jpg" mode=""></image>
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

        <!-- 电话服务盒子 -->
        <view class="iphone">
          <!-- 电话 -->
          <view class="telephone">
            <image src="../../static/icon/93.png" mode=""></image>
            <view class="">
              电话
            </view>
          </view>
          <!-- 服务 -->
          <view class="telephone">
            <image src="/static/icon/3.png" mode=""></image>
            <view class="">
              服务
            </view>
          </view>

        </view>

      </view>

      <button class="count">我的账单</button>
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

      .collect {
        padding-left: 20rpx;
        image {
          width: 50rpx;
          height: 50rpx;
          margin-top: 20rpx;
        }
      }

      // 历史
      .clear {
        display: flex;
        justify-content: center;
        align-items: center;
        padding-right: 20rpx;

        image {
          width: 50rpx;
          height: 50rpx;
          margin-top: 20rpx;
        }
        text{
          padding-left: 10rpx;
          box-sizing: border-box;
        }
      }
    }



    .shop {
      width: 94%;
      height: 900rpx;
      margin: 20rpx auto;
      // background-color: pink;

      // 图片上面的两条信息
      .info {
        width: 100%;
        height: 120rpx;
        // background-color: yellowgreen;
        padding-left: 30rpx;
        .infos {
          font-size: 26rpx;
          
          image {
            width: 40rpx;
            height: 40rpx;
          }
          text{
            padding-left: 15rpx;
          }
        }
      }

      image {
        width: 100%;
        height: 500rpx;
      }

      .price {
        width: 100%;
        // background-color: aqua;
        // height: 180rpx;
        display: flex;
        justify-content: space-between;

        .uname {
          padding-left: 30rpx;
          margin-top: 5rpx;
        }

        .iphone {
          padding-right: 20rpx;
          margin-top: 5rpx;
          // background-color: rebeccapurple;
          width: 200rpx;
          display: flex;
          justify-content: space-between;

          .telephone {
            image {
              width: 50rpx;
              height: 50rpx;
            }
          }
        }
      }


      // 我的账单按钮
      button {
        width: 80%;
        height: 75rpx;
        background-color: crimson;
        color: #f5f5f5;
        margin-top: 20rpx;
      }

    }

  }
</style>
