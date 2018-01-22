<template>
  <article>
    <Slider :items="items" :cname="$style.slider" />
    <section :class="$style.list">
      <div :class="$style.item" v-for="item in enters" :key="item.img">
        <router-link :to="{ name: item.href }">
          <img :src="item.img" :alt="item.title">
          <h4>{{ item.title }}</h4>
        </router-link>
      </div>
    </section>
  </article>
</template>

<script>
import Slider from '../core/slider';

export default {
  components: {
    Slider,
  },
  data() {
    return {
      items: [{
        href: 'home',
        src: '//img12.360buyimg.com/jrpmobile/jfs/t15766/20/1888396674/25048/1c352a11/5a65be55Ne6e47009.jpg?width=750&height=400',
      }, {
        href: 'home',
        src: '//img12.360buyimg.com/jrpmobile/jfs/t18085/349/231675830/46722/e4fcfccc/5a65be71N1b582948.jpg?width=750&height=400',
      }, {
        href: 'home',
        src: '//img12.360buyimg.com/jrpmobile/jfs/t15955/19/1871278384/42272/7fa9b385/5a65be93N9f79daae.jpg?width=750&height=400',
      }, {
        href: 'home',
        src: '//img12.360buyimg.com/jrpmobile/jfs/t16696/115/233669791/26400/99648bf2/5a65bf13N6599dbe1.jpg?width=750&height=400',
      }],
      enters: [{
        href: 'home',
        img: '//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132',
        title: '优惠券',
      }, {
        href: '',
        img: '//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132',
        title: '领红包',
      }, {
        href: 'home',
        img: '//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132',
        title: '抢钢镚',
      }, {
        href: 'home',
        img: '//img12.360buyimg.com/jrpmobile/jfs/t4618/115/2179710654/11347/bf520df/58ec9d84Nfd169001.png?width=132&height=132',
        title: '领京豆',
      }, {
        href: 'home',
        img: '//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135',
        title: '白条提额',
      }],
    };
  },
}
</script>

<style lang="scss" module>
@import '../../css/element.scss';

.slider {
  margin-top: 120px;
  img {
    width: 100%;
  }
}

.list {
  @include list(row);
  background: #fff;
  padding-top: 40px;
  padding-bottom: 20px;
  justify-content: space-around;
  a {
    text-decoration: none;
  }
  .item {
    text-align: center;
    img {
      display: inline-block;
      width: 90px;
      height: 90px;
    }
    h4 {
      font-size: 26px;
      margin-top: 12px;
      color: #666;
    }
  }
}

</style>


