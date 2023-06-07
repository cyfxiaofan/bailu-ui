# Button

This is a button component

## Basic Usage

:::demo You can set `primary` 、 `success`、 `warning`、 `danger` 、`default` type for button.

```vue
<template>
  <lu-space>
    <lu-button type="default">Default</lu-button>
    <lu-button type="primary">Primary</lu-button>
    <lu-button type="success">Success</lu-button>
    <lu-button type="warning">Warning</lu-button>
    <lu-button type="danger">Danger</lu-button>
  </lu-space>
</template>
```

:::

## Plain Style

:::demo You can set `plain` style for button.

```vue
<template>
  <lu-space>
    <lu-button plain>Default</lu-button>
    <lu-button type="primary" plain>Primary</lu-button>
    <lu-button type="success" plain>Success</lu-button>
    <lu-button type="warning" plain>Warning</lu-button>
    <lu-button type="danger" plain>Danger</lu-button>
  </lu-space>
</template>
```

:::

## Disabled State

:::demo You can set `disabled` state for button.

```vue
<template>
  <lu-space>
    <lu-button disabled>Default</lu-button>
    <lu-button type="primary" disabled>Primary</lu-button>
    <lu-button type="success" disabled>Success</lu-button>
    <lu-button type="warning" disabled>Warning</lu-button>
    <lu-button type="danger" disabled>Danger</lu-button>
  </lu-space>

  <lu-space class="vp-mt-2">
    <lu-button disabled plain>Default</lu-button>
    <lu-button type="primary" disabled plain>Primary</lu-button>
    <lu-button type="success" disabled plain>Success</lu-button>
    <lu-button type="warning" disabled plain>Warning</lu-button>
    <lu-button type="danger" disabled plain>Danger</lu-button>
  </lu-space>
</template>
```

:::

## Button Size

:::demo You can set `mini` 、 `small`、 `default` 、`large` size for button.

```vue
<template>
  <lu-space>
    <lu-button size="mini" type="primary">Mini</lu-button>
    <lu-button size="small" type="primary">Small</lu-button>
    <lu-button type="primary">Default</lu-button>
    <lu-button size="large" type="primary">Large</lu-button>
  </lu-space>
</template>
```

:::

## Button Shape

:::demo You can set `default` 、 `circle`、 `round` shape for button.

```vue
<template>
  <lu-space>
    <lu-button shape="default" type="primary">Default</lu-button>
    <lu-button shape="round" type="primary">Round</lu-button>
    <lu-button type="primary" icon-size="15px" icon="TrashEmpty"></lu-button>
    <lu-button shape="circle" type="primary" icon-size="15px" icon="SearchGlass"></lu-button>
  </lu-space>
</template>
```

:::

## Icon Button

:::demo You can set `icon` for button.

```vue
<template>
  <lu-space>
    <lu-button type="primary" icon-size="15px" icon="SearchGlass"></lu-button>
    <lu-button type="primary" icon-size="15px" icon="EditPencil01"></lu-button>
    <lu-button type="primary" icon-size="15px" icon="ShareAndroid"></lu-button>
    <lu-button type="primary" icon-size="15px" icon="TrashEmpty">删除</lu-button>
  </lu-space>
</template>
```

:::

## Loading State

:::demo You can set `loading` state for button.

```vue
<template>
  <lu-space class="vcenter">
    <lu-button loading>Default</lu-button>
    <lu-button type="primary" loading>Primary</lu-button>
    <lu-button type="success" loading>Success</lu-button>
    <lu-button shape="circle" loading type="primary" icon-size="15px" icon="SearchGlass"></lu-button>
    <lu-button :loading="loading" @click="loadingClick" type="primary" icon="AddPlus">Click Me</lu-button>
  </lu-space>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const loading = ref<boolean>(false)

const loadingClick = () => {
  loading.value = true
  setTimeout(() => {
    loading.value = false
  }, 2000)
}
</script>
```

:::

## Props

| Name      | Description    | Type                                                         | Default |
| --------- | -------------- | ------------------------------------------------------------ | ------- |
| type      | button type    | `primary` \| `success` \| `warning` \| `danger` \| `default` | default |
| size      | button size    | `mini` \| `small` \| `default` \| `large`                    | default |
| shape     | button shape   | `default` \| `circle` \| `round`                             | default |
| plain     | plain style    | boolean                                                      | false   |
| disabled  | disabled state | boolean                                                      | false   |
| loading   | loading state  | boolean                                                      | false   |
| icon      | icon name      | string                                                       | -       |
| iconColor | icon color     | string                                                       | -       |
| iconSize  | icon size      | string                                                       | -       |

## Events

| Name  | Description                         |
| ----- | ----------------------------------- |
| click | emitted when the button is clicked. |

## Slots

| Name    | Description     | Type | Subtags |
| ------- | --------------- | ---- | ------- |
| default | button content  | any  | -       |
| loading | loading content | any  | -       |
| icon    | icon content    | any  | -       |

<!-- ## Directives

| Name | Description | Type |
| ---- | ----------- | ---- |
| v-loading | show animation while loading data | boolean | -->
