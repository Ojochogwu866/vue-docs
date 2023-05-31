<template>
  <c-v-stack>
    <c-input-group>
      <c-input-left-addon> https:// </c-input-left-addon>
      <c-input placeholder="website.com" />
      <c-input-right-addon> .com </c-input-right-addon>
    </c-input-group>

    <c-input-group>
      <c-input-left-addon> +234 </c-input-left-addon>
      <c-input placeholder="814-002-40" />
    </c-input-group>
  </c-v-stack>
</template>

<script setup>
import {
  CInput,
  CInputGroup,
  CInputRightAddon,
  CInputLeftAddon
} from '@chakra-ui/vue-next';
</script>
