<template>
  <div>
    <div class="recommend-title">
      周末去哪
    </div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/4e/3e87ee62e59cdb.jpg_r_640x214_fe6cc902.jpg',
        title: '千岛湖伯爵号',
        desc: '浙江省杭州市淳安县千岛湖镇旅游码头'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9f/7d45cc38259e0.jpg_r_640x214_156f4299.jpg',
        title: '杭州云曼温泉',
        desc: '杭州市萧山区风情大道第一世界'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/ae/4fe23c6b6679e2.jpg_r_640x214_368a18d8.jpg',
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
  .item-img-wrapper {
    overflow: hidden;
    height: 0;
    padding-bottom: 33.9%;
  }
  .item-img {
    width: 100%;
  }
  .item-info {
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
</style>
