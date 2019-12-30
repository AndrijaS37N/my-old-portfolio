<template>
  <h1>{{ message }}</h1>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class Message extends Vue {
  @Prop() private message!: string;
}
</script>