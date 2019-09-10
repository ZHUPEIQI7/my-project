<template>
  <div class="about">
    <h1>This is an about page</h1>
    <demo msg="这是About传送给demo的话" />
  </div>
</template>

<script lang="ts">
import { Component, Vue} from 'vue-property-decorator';
import demo from '@/components/demo.vue';

@Component({
  components:{
    demo,
  },
})

export default class About extends Vue {}
</script>