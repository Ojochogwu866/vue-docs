<template>
  <c-v-stack>
    <c-input-group>
      <c-input-left-element color="gray.300"> $ </c-input-left-element>
      <c-input placeholder="Enter amount" />
    </c-input-group>
    <c-input-group>
      <c-input-right-element>
        <c-icon name="check" color="green.500" />
      </c-input-right-element>
      <c-input placeholder="Name of identified pet" />
    </c-input-group>
  </c-v-stack>
</template>
<script setup>
import {
  CInput,
  CIcon,
  CInputRightElement,
  CInputGroup,
  CInputLeftElement
} from '@chakra-ui/vue-next';
</script>
