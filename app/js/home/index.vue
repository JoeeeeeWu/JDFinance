<template lang="html">
    <div>
        <Header />
        <Slider />
        <Novice />
    </div>
</template>

<script>
import Header from '../public/header';
import Slider from './hslider';
import Novice from './novice';

export default {
  components: {
    Header,
    Slider,
    Novice,
  },
}
</script>

<style lang="scss" module>
  
</style>
