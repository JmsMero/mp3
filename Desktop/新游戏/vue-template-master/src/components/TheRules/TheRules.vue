<!-- 规则 -->
<template>
  <div class="the_rules">
    <p>规则</p>
  </div>
</template>

<script>
export default {
  name: 'TheRules',
  props: {
    prizeList: { // 奖品列表
      type: Array,
      required: true
    },
    width: {
      required: true
    },
    height: {
      required: true
    },
    borderColor: { // 每一块扇形的外边框颜色
      type: String,
      default: 'rgba(255,255,255,0)'
    },
    turnsNumber: { // 转动的圈数
      type: Number,
      default: 5
    },
    turnsTime: { // 转动持续时间（秒）
      type: Number,
      default: 5
    }
  },
  data() {
    return {
    }
  },
  methods: {
  },
  mounted() {
  },
}

</script>
<style lang="scss" scoped>
  .the_rules{
    p{
      font-size: 20px;
    }
  }
</style>
