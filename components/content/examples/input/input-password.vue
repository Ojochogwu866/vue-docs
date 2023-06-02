<template>
  <c-input-group size="md">
    <c-input
      :type="show ? 'text' : 'password'"
      placeholder="Enter password"
      :value="password"
    />
    <c-input-right-element width="4.5rem">
      <c-button height="1.75rem" size="sm" @click="handleVisibility">
        {{ show ? 'Hide' : 'Show' }}
      </c-button>
    </c-input-right-element>
  </c-input-group>
</template>
<script setup>
import { ref } from 'vue';

const password = ref('');
const show = ref(false);

function handleVisibility() {
  show.value = !show.value;
}
</script>
