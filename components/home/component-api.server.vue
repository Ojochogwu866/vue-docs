<template>
  <c-container max-w="8xl" my="20">
    <c-grid :template-columns="{ base: '1fr', sm: '1.5fr 1fr' }" max-w="50%">
      <c-stack spacing="5">
        <chakra.p
          :color="useColorModeValue('emerald.600', 'emerald.50').value"
          font-weight="bold"
          >Powerful Developer Experience</chakra.p
        >
        <c-heading> Develop with an open, extendable API </c-heading>
        <chakra.p>
          Chakra UI Vue components can be customized at any level - whether it's
          at the component level, or the theme level. You can also extend the
          components to add new features, or override existing ones.
        </chakra.p>
        <c-grid
          gap="4"
          :w="{ base: 'full', sm: 'fit-content' }"
          :template-columns="{ base: 'repeat(1, 1fr)', sm: 'repeat(4, auto)' }"
        >
          <c-stack
            v-for="(feature, i) in features"
            :key="i"
            :border="
              useColorModeValue(
                '1px solid rgba(47, 43, 67, 0.1)',
                '1px solid var(--chakra-colors-whiteAlpha-200)'
              ).value
            "
            :box-shadow="
              useColorModeValue(
                // '0px 1px 3px rgba(47, 43, 67, 0.1), inset 0px -1px 0px rgba(47, 43, 67, 0.1)',
                'none',
                'none'
              ).value
            "
            px="4"
            py="5"
            rounded="12px"
            align-items="flex-start"
            :w="{ base: 'full', sm: '250px' }"
          >
            <chakra.svg
              :color="`${
                useColorModeValue('emerald.600', 'white').value
              } !important`"
              font-size="1.8em"
              :as="feature.icon"
            />
            <chakra.h3
              :color="useColorModeValue('emerald.600', 'white').value"
              font-weight="bold"
              font-size="1.1rem"
            >
              {{ feature.title }}
            </chakra.h3>
            <chakra.p>
              {{ feature.description }}
            </chakra.p>
          </c-stack>
        </c-grid>
      </c-stack>
      <c-center />
    </c-grid>
  </c-container>
</template>

<script setup lang="ts">
import { chakra, useColorModeValue } from '@chakra-ui/vue-next';
import AccessibilityIcon from '../icons/accessibility-icon';
import ComposableIcon from '../icons/composable-icon';
import ThemeIcon from '../icons/theme-icon';
import StateMachineIcon from '../icons/state-machine-icon';

const features = [
  {
    icon: AccessibilityIcon,
    title: 'Accessibility',
    description:
      'Chakra UI strictly follows WAI-ARIA standards for all components.'
  },
  {
    icon: ThemeIcon,
    title: 'Design System friendly',
    description:
      'Customize any part of our components to match your design needs.'
  },
  {
    icon: StateMachineIcon,
    title: 'State Machine Driven',
    description:
      'Built with UI state machines for predictable and reliable UI. Powered by Zag.js'
  },
  {
    icon: ComposableIcon,
    title: 'Composable',
    description:
      'Designed with composition in mind. Compose new components with ease.'
  }
];
</script>
