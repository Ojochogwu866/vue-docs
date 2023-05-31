---
title: Input
description: Input Component
version: 2.0+
---

# Input

The `input` component is used to get text in the input field.

## Usage

Chakra-ui Vue exports the following components;

- **CInput**: The input container that holds the input text.
- **CInputGroup**: The `CInputGroup` component is a container to enhance an input by adding an icon, text or a button on either sides of the container.

```js
import { CInput, CInputGroup } from '@chakra-ui/vue-next';
```

### Base input

Here's a basic usage format of the `input` component

::showcase
::basic-usage
::
::

```html
<c-input placeholder="Hello" />
```

### Input Sizes

The `input` component comes with three sizes, the default size is `md`.

- `sm (32px)`
- `md (40px)`
- `lg (48px)`

::showcase
::input-sizes
::
::

```html
<c-v-stack spacing="3">
  <c-input v-model="input" placeholder="small size" size="sm" />
  <c-input v-model="input" placeholder="medium size" size="md" />
  <c-input v-model="input" placeholder="large size" size="lg" />
</c-v-stack>
```

### Input variants

The `input` component has four differepnt variant styles `outlined`, `flushed`, `filled`, and
`unstyled`. You can use any of the variants by passing the appropriate prop.

::showcase
::input-variants
::
::

```html
<c-v-stack>
  <c-input variant="outline" placeholder="Outline" />
  <c-input variant="filled" placeholder="Filled" />
  <c-input variant="flushed" placeholder="Flushed" />
  <c-input variant="unstyled" placeholder="Unstyled" />
</c-v-stack>
```

### Input addons

Addons can be added on either sides of the input component to enhance flexibility of the interface.

::showcase
::input-addons
::
::

```html
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
```

### Input elements

Elements like icons and buttons can be added in the input tabs. This can easily be done by exporting the `c-input-left-element` and `c-input-right-element` in your `c-input-group` component. Moreso, you can pass properties to customize color of icon elements.

::showcase
::input-elements
::
::

```html
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
```
