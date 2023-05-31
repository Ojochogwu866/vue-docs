<template>
  <c-v-stack>
    <c-input variant="outline" placeholder="Outline" />
    <c-input variant="filled" placeholder="Filled" />
    <c-input variant="flushed" placeholder="Flushed" />
    <c-input variant="unstyled" placeholder="Unstyled" />
  </c-v-stack>
</template>
<script setup>
import { CInput } from '@chakra-ui/vue-next';
</script>
