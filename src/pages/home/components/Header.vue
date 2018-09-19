<template>
    <div class="header">
      <div class="header-left">
        <div class="iconfont back-icon">&#xe624;</div>
      </div>
      <div class="header-input">
        <span class="iconfont">&#xe632;</span>
        请输入城市/景点/游玩主题
      </div>
      <router-link to="/city">
        <div class="header-right">
          {{this.city}}
          <span class="iconfont arrow-icon">&#xe64a;</span>
        </div>
      </router-link>
    </div>
</template>

<script>
import {mapState} from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>
<!--scoped>保证样式为局部样式，不会对其他组件产生影响-->
<!--1rem = html font-size = 50px;-->
<style scoped>
  .header {
    display: flex;
    line-height: .86rem;
    background: #00bcd4;
    color: #fff;
  }
  .header-left {
    width: .64rem;
    float: left;
  }
  .back-icon {
    text-align: center;
    font-size: .4rem;
  }
  .header-input {
    flex: 1;
    height: .64rem;
    line-height: .60rem;
    margin-top: .12rem;
    margin-left: .2rem;
    padding-left: .2rem;
    background: #fff;
    color: #999;
    border-radius: .1rem;
  }
  .header-right {
    min-width: 1.04rem;
    padding: 0 0.1rem;
    float: right;
    text-align: center;
    color: #ffffff;
  }
  .arrow-icon {
    margin-left: -0.04rem;
    font-size: .24rem;
  }
</style>
