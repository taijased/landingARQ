<template>
  <svg xmlns="http://www.w3.org/2000/svg"
    :width="width"
    :height="height"
    viewBox="0 0 77 77"
    version="1.1"
    xmlns:xlink="http://www.w3.org/1999/xlink"
    role="presentation"
  >
    <title>arq-logo</title>
    <desc>Created with Sketch.</desc>
    <defs>
      <linearGradient x1="23.7597516%" y1="11.4791801%" x2="75.8431271%" y2="50%" id="linearGradient-1">
        <stop stop-color="#3736C1" stop-opacity="0" offset="0%"></stop>
        <stop stop-color="#3736C1" offset="100%"></stop>
      </linearGradient>
    </defs>
    <g id="arq-logo" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
      <path d="M77,38.5 C77,59.7626944 59.7626944,77 38.5,77 C17.2373056,77 0,59.7626944 0,38.5 C0,17.2373056 17.2373056,0 38.5,0 C59.7626944,0 77,17.2373056 77,38.5" id="Fill-1" fill="#3D3BEE"></path>
      <path d="M38.3333333,0 C31.2884815,0 24.6882963,1.88543056 19,5.16327778 C30.5548889,11.8216389 38.3333333,24.2517917 38.3333333,38.5 C38.3333333,52.7482083 46.1117778,65.1783611 57.6666667,71.8356528 C63.356037,75.1145694 69.9551481,77 77,77 L77,38.5 C77,17.2373056 59.6880741,0 38.3333333,0 Z" id="Clip-4" fill="url(#linearGradient-1)"></path>
    </g>
  </svg>
</template>

<script>
export default {
  props: {
    width: {
      type: [Number, String],
      default: 77
    },
    height: {
      type: [Number, String],
      default: 77
    }
  }
}
</script>


