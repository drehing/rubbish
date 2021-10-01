<template>
    <div
    class="demo-shadow"
    :style="{ boxShadow: `var(--el-box-shadow-base)` }"
    ></div>
    <span class="demo-shadow-text"
    >Basic Shadow
    <code>box-shadow: 'xxx'</code></span
    >
</template>

<script>
export default {
  data() {
    return {
      shadowGroup: [
        {
          name: 'Basic Shadow',
          type: 'base',
        },
        {
          name: 'Light Shadow',
          type: 'light',
        },
      ],
    }
  },
  methods: {
    getValue(type) {
      const getCssVarValue = (prefix, type) =>
        getComputedStyle(document.documentElement).getPropertyValue(
          `--el-${prefix}-${type}`
        )
      return getCssVarValue('box-shadow', type)
    },
  },
}
</script>
<style scoped>
.demo-shadow {
  height: 100px;
  width: 50%;
  border: 1px solid var(--el-border-color-base);
}
.demo-shadow-text {
  line-height: 50px;
  color: var(--el-text-color-regular);
  font-size: 14px;
}
</style>
