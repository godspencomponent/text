<template>
  <div class="component" v-html="scopeGet('text')"></div>
</template>

<script>
  import {VueExtend} from 'godspen-lib'

  export default {
    mixins: [VueExtend.mixin],
    name: 'text',
    label: process.env.LABEL,
    style: process.env.STYLE,
    leaf: true, // 是否是叶子节点，为true的时候该节点下面不能添加节点
    props: {
      text: {
        type: [String, Number],
        editer: {
          type: 'text',
          label: '文字内容',
          desc: '具体的内容数据'
        },
        default: '默认文字'
      }
    },
    computed: {
    },
    editorMethods: {
    },
    methods: {
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus" type="text/stylus" scoped>
  .component {
    width: 100%;
    height: auto;
  }
</style>
