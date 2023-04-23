<template>
  <view class="base">
    <!-- 搜索框 -->
    <view class="search">
      <input type="text" placeholder="搜美食,菜谱">
      <image src="../../static/icon/3.png" mode=""></image>
    </view>

    <!-- 先在外面包一个大盒子 -->
    <view class="container">
      <!-- 左侧滑动区域   滑动在小程序里面用scroll-view组件  纵向的设置一个属性为scroll-y -->
      <!-- 给左侧滑动区域 动态绑定样式 -->
      <scroll-view class="left" scroll-y>
        <!-- 因为左侧一级分类列表全是文字所以用 block在外面包裹一下 到时候发完请求用v-for循环就不用写那么多view -->
        <view class="left-item">
          白酒
        </view>
        <view class="left-item">
          啤酒
        </view>
        <view class="left-item">
          红酒
        </view>
        <view class="left-item">
          饮料
        </view>

      </scroll-view>
      
      <!-- 右侧滑动区域 -->
      <scroll-view class="right-scroll-view" scroll-y>
        <view class="cate-lv2">
          <!-- 二级分类列表的标题 -->
          <view class="cate-lv2-title">白酒</view>
          <!-- 三级分类的列表最大盒子 -->
          <view class="cate-lv3-list">
            <!-- 图片+文字盒子 -->
            <view class="cate-lv3-item">
              <!-- 图片 -->
             <image src="/static/maotai.jpg" mode=""></image>
             <!-- 文字 -->
             <view class="word">
               <view class="goodsName">
                 贵州茅台
               </view>
               <view class="number">
                 ￥100/瓶
               </view>
             </view>
            </view>
            
            <!-- 增加减少数量按钮盒子 -->
            <view class="cate-lv3-item2">
              <image src="/static/reduce.png" mode=""></image>
              <text>2</text>
              <image src="../../static/add.png" mode=""></image>
            </view>
          
          </view>
        </view>
      </scroll-view>

    </view>
    
    
    <!-- 最后一行 -->
    <view class="choose">
      <view class="choose_left">
        <navigator url="" open-type="switchTab">
           <image src="/static/icon/icon_car.png" mode="" class="car"></image>
        </navigator>
       
        <view class="fashion">
          
          <text>
            ￥300
          </text>
        </view>
      </view>
    
      <button>
        购买
      </button>
    </view>
    
    
  </view>
</template>

<script>
  export default {
    data() {
      return {

      };
    },




  }
</script>

<style lang="scss">
  .base {
    background-color: #f5f5f5;

    .search {
      width: 94%;
      height: 80rpx;
      // background-color: pink;
      margin: 0 auto;
      position: relative;

      input {
        width: 100%;
        height: 80rpx;
        background-color: #f5f5f5;
        border-radius: 50rpx;
        border: 1px solid gray;
        padding-left: 80rpx; //专门用来调节input默认的 placeholder备注语言的距离
        box-sizing: border-box;
      }

      image {
        width: 50rpx;
        height: 50rpx;
        position: absolute;
        left: 20rpx;
        top: 10rpx;
      }
    }


    // 左侧一级导航
    .container {
      // 变为左右两侧
      display: flex;
      background-color: red;
      margin: 30rpx auto;

      .left {
        // 给一个固定的宽可以用px
        width: 120px;
        background-color: aqua;

        .left-item {
          font-size: 30rpx;
          background-color: #f7f7f7;
          line-height: 60px;
          text-align: center;



        }
      }
    }
    
    
    // 二级分类列表的标题
    .cate-lv2-title{
      font-size: 15px;
      font-weight: bold;
      // text-align: center;
      padding: 40rpx 0 0 30rpx;
    }
    
    .right-scroll-view{
      background-color: #ffffff;
    }
    
    
    .cate-lv3-list{
      display: flex;  
      justify-content: space-between;
      // flex-wrap: wrap;  // 让横向排列的图片换行显示 
      
      // 三级分类的 item 项
      .cate-lv3-item{
        display: flex;
        // background-color: aqua;
        // flex-direction: column;  //设置图片纵向排列
        // justify-items: center;   // 设置图片横向居中
        // align-items: center;    //设置图片纵向居中
        // margin-bottom: 10px;
        image{
          width: 250rpx;
          height: 300rpx;
        }
        
        .word{
          // background-color: pink;
          .goodsName{
            font-size: 35rpx;
            font-weight: bold;
          }
          .number{
            color: red;
          }
        }
       
      }
      
      .cate-lv3-item2{
        display: flex;
        // background-color: burlywood;
       margin-top: 200rpx;
        image{
          width: 70rpx;
          height: 70rpx;
        }
        text{
          font-size: 40rpx;
        }
      }
    }
    
    // 最后一行
    .choose {
      display: flex;
      width: 100%;
      background-color: rgb(255, 255, 255);
      box-shadow: #fffff;
      height: 150rpx;
      margin-top: 20rpx;
      color: #ffffff;
      position: fixed;
      bottom: 0rpx;
    
      .choose_left {
        display: flex;
        align-items: center;
        width: 70%;
    
        image {
          width: 100rpx;
          height: 100rpx;
        }
      }
    
      .car {
        margin: 5rpx 0 0 10rpx;
      }
    
      .fashion {
        // display: flex;
        // flex-direction: column;
        justify-content: space-evenly;
        margin-left: 10rpx;
        text{
          font-size: 40rpx;
          color: #000000;
        }
      }
    
      button {
        width: 30%;
        margin: 0;
        padding: 0;
        background-color: red;
        color: #ffffff;
        // float: right;
        line-height: 150rpx;
        text-align: center;
      }
    }
  }
</style>
