<template>
    <div class="demo">
        <h3>I'am a component of About page . My name is "Demo"!</h3>
        <h2>{{msg}}</h2>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class demo extends Vue{
    @Prop() private msg!: string;
}
</script>