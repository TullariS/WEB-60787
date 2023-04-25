<template>
  <p>
    {{ prop1.strVar }}
    {{ prop2.strVar2 }}
    {{ prop1Obj.strVar }}
    {{ prop2Obj.strVar2 }}
  </p>
</template>
<script lang="ts">
import { PropType } from 'vue'
import Prop2 from './types'

// noinspection JSUnusedGlobalSymbols
export default {
  props: {
    prop1: Object as PropType<{strVar: string | string[]}>,
    prop2: Object as PropType<Prop2>,
  },
  data () {
    return {
      prop1Obj: this.prop1,
      prop2Obj: this.prop2,

      prop1Val: this.prop1.strVar,
      prop2Val: this.prop2.strVar2,
    }
  },
}
</script>