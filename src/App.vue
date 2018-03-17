<template>
  <div>
    <kashikoma></kashikoma>
    <p v-if="msg.length > 0">{{msg}}</p>
    <p v-else>ぷしゅーしたらダメぷり</p>
    <input type="text" v-model="msg">
    <button @click="clear()">消しちゃうぷりー</button>
  </div>
</template>

<script>
import kashikoma from './components/kashikoma'

export default {
  components: {
    kashikoma
  },
  data () {
    return {
      msg: 'ぷりぷりかしこまぷしゅー'
    }
  },
  methods: {
    clear () {
      this.msg = ''
    }
  }
  // 一旦別枠で考えることにする
  // mounted: function () {
  //   // var that = this
  //   $.getJSON('http://zipcloud.ibsnet.co.jp/api/search?zipcode=1500001', {}, function (json) {
  //     console.log(json)
  //   })
  // }
}
</script>
