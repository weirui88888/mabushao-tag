<template>
    <div id="app">
        <mbs-tag
        v-bind="{disabled, type, size, addBtn, max, tagKey, maxLength}"
        v-model="list"
        @add="onAdd"
        @delete="ondel"
        @input="change"/>
    </div>
  </template>

<script>
import mbsTag from './component/index'
export default {
  name: 'app',
  data () {
    return {
      description: 'demo',
      tagKey: 'title',
      disabled: false,
      addBtn: '添加规则',
      type: '',
      size: 'medium',
      max: 5, // 最多添加
      maxLength: 10, // 文本长度
      list: [
        { title: '111' },
        { title: '2222' }
      ]
    }
  },
  components: {
    mbsTag
  },
  methods: {
    change (obj) {
      console.log(obj)
    },
    onAdd (obj) {
      console.log(obj)
    },
    ondel (obj) {
      console.log(obj)
    }
  }
}
</script>

  <style>

  </style>
