<template>
  <div>
    <div class="recommend-title">
      热销推荐
    </div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201305/27/564904f316afb3b1c8d65eac.jpg_200x200_dd2b194e.jpg',
        title: '千岛湖伯爵号',
        desc: '浙江省杭州市淳安县千岛湖镇旅游码头'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201401/06/3fbbddda915cb7637439d484440d36be.jpg_200x200_a54e87dd.jpg',
        title: '杭州云曼温泉',
        desc: '杭州市萧山区风情大道第一世界'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201406/23/6a12f3746bdb338390706f3d7ac34f87.jpg_200x200_86db3cde.jpg',
        title: '千岛湖白云溪漂流',
        desc: '浙江省杭州市淳安县千岛湖镇宋村乡'
      }]
    }
  }
}
</script>

<style scoped>
  .recommend-title {
    margin-top: .2rem;
    line-height: .8rem;
    background: #eee;
    text-indent: .2rem;
  }
  .item {
    overflow: hidden;
    display: flex;
    height: 1.9rem;
  }
  .item-img {
    width: 1.7rem;
    height: 1.7rem;
    padding: .1rem;
  }
  .item-info {
    flex: 1;
    min-width: 0;
    padding: .1rem;
  }
  .item-title {
    line-height: .54rem;
    font-size: .32rem;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
  }
  .item-desc {
    line-height: .4rem;
    color: #999;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
  }
  .item-button {
    line-height: .44rem;
    margin-top: .16rem;
    background: #ff9300;
    padding: 0 .1rem;
    border-radius: 0.06rem;
    color: #ffffff;
  }
</style>
