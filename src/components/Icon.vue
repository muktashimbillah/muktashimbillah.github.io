<template>
  <span class="icon" :style="containerStyle" aria-hidden="true">
    <svg
      v-if="name === 'github'"
      :width="size"
      :height="size"
      viewBox="0 0 24 24"
      :fill="fill">
      <path
        d="M12 2C6.48 2 2 6.48 2 12c0 4.42 2.87 8.17 6.84 9.49.5.09.68-.22.68-.48v-1.7c-2.78.6-3.37-1.34-3.37-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.61.07-.61 1 .07 1.53 1.03 1.53 1.03.89 1.52 2.34 1.08 2.91.83.09-.65.35-1.09.63-1.34-2.22-.25-4.55-1.11-4.55-4.94 0-1.09.39-1.98 1.03-2.68-.1-.25-.45-1.27.1-2.64 0 0 .84-.27 2.75 1.02A9.56 9.56 0 0112 6.8c.85 0 1.71.12 2.51.34 1.91-1.29 2.75-1.02 2.75-1.02.55 1.37.2 2.39.1 2.64.64.7 1.03 1.59 1.03 2.68 0 3.84-2.34 4.68-4.57 4.93.36.31.68.92.68 1.85v2.74c0 .27.18.58.69.48C19.14 20.16 22 16.42 22 12c0-5.52-4.48-10-10-10z" />
    </svg>

    <svg
      v-else-if="name === 'linkedin'"
      :width="size"
      :height="size"
      viewBox="0 0 24 24"
      :fill="fill">
      <path
        d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6zM2 9h4v12H2z" />
      <circle cx="4" cy="4" r="2" />
    </svg>

    <svg
      v-else-if="name === 'download'"
      :width="size"
      :height="size"
      viewBox="0 0 24 24"
      fill="none"
      :stroke="stroke"
      :stroke-width="strokeWidth"
      stroke-linecap="round"
      stroke-linejoin="round">
      <path d="M21 15v4a2 2 0 01-2 2H5a2 2 0 01-2-2v-4" />
      <polyline points="7 10 12 15 17 10" />
      <line x1="12" y1="15" x2="12" y2="3" />
    </svg>

    <svg
      v-else-if="name === 'external'"
      :width="size"
      :height="size"
      viewBox="0 0 24 24"
      fill="none"
      :stroke="stroke"
      :stroke-width="strokeWidth"
      stroke-linecap="round"
      stroke-linejoin="round">
      <path d="M18 13v6a2 2 0 01-2 2H6a2 2 0 01-2-2V8a2 2 0 012-2h6" />
      <polyline points="15 3 21 3 21 9" />
      <line x1="10" y1="14" x2="21" y2="3" />
    </svg>

    <svg
      v-else-if="name === 'arrow-right'"
      :width="size"
      :height="size"
      viewBox="0 0 24 24"
      fill="none"
      :stroke="stroke"
      :stroke-width="strokeWidth"
      stroke-linecap="round"
      stroke-linejoin="round">
      <line x1="5" y1="12" x2="19" y2="12" />
      <polyline points="12 5 19 12 12 19" />
    </svg>

    <span v-else-if="name === 'email'" :style="textStyle">✉</span>
    <span v-else-if="name === 'whatsapp'" :style="textStyle">💬</span>

    <svg
      v-else-if="name === 'menu'"
      :width="size"
      :height="size"
      viewBox="0 0 24 24"
      fill="none"
      :stroke="stroke"
      :stroke-width="strokeWidth"
      stroke-linecap="round"
      stroke-linejoin="round">
      <line x1="3" y1="12" x2="21" y2="12" />
      <line x1="3" y1="6" x2="21" y2="6" />
      <line x1="3" y1="18" x2="21" y2="18" />
    </svg>
  </span>
</template>

<script>
export default {
  name: "Icon",
  props: {
    name: {
      type: String,
      required: true,
    },
    size: {
      type: [Number, String],
      default: 14,
    },
    fill: {
      type: String,
      default: "currentColor",
    },
    stroke: {
      type: String,
      default: "currentColor",
    },
    strokeWidth: {
      type: [Number, String],
      default: 2.5,
    },
    className: {
      type: String,
      default: "",
    },
  },
  computed: {
    containerStyle() {
      return {
        display: "inline-flex",
        alignItems: "center",
        justifyContent: "center",
      };
    },
    textStyle() {
      return {
        display: "inline-flex",
        alignItems: "center",
        justifyContent: "center",
        width: typeof this.size === "number" ? `${this.size}px` : this.size,
        height: typeof this.size === "number" ? `${this.size}px` : this.size,
        fontSize: typeof this.size === "number" ? `${this.size}px` : this.size,
      };
    },
  },
};
</script>

<style scoped>
.icon {
  display: inline-flex;
  align-items: center;
  justify-content: center;
}
</style>
