<style lang="scss">
  @import "./dialog";
</style>
<style lang="scss" scoped="">
  @import "../functions";

  .dialog__inner {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
</style>
<template>
  <modal :modal="modal" :mask="mask" :visible="modal_show" class="dialog__wrap">
    <div class="dialog__inner">
      <slot>
        <template v-if="type=='loading'">
          <img class="window__icon loading__icon" src="./images/loading@3x.png"/>
        </template>
        <template v-if="type=='success'">
          <img class="window__icon" src="./images/success@3x.png"/>
        </template>
        <template v-if="type=='fail'">
          <img class="window__icon" src="./images/fail@3x.png"/>
        </template>
      </slot>
      <slot name="text">
        <div class="dialog__text" v-if="inner_text">{{ inner_text }}</div>
      </slot>
    </div>
  </modal>
</template>
<script>
  import Mixins from './_mixins'

  export default {
    name: 'Loading',
    props: {
      type: {
        type: String,
        default: 'loading'
      },
      text: {
        type: String,
        default: ''
      }
    },
    methods:{

      setText (text) {
        this.inner_text = text
        return this
      },
    }
  }
</script>