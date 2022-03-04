<template>
  <div>
    <a class="animated-link" :href="link.url">{{ link.text }}</a>
  </div>
</template>

<script>
export default {
  props: {
    link: {
      type: Object,
      default: {
        url: "#",
        text: "Dummy link goes here",
      },
    },
  },
};
</script>

<style>
a.animated-link {
  color: inherit;
  font-size: 16px;
  font-weight: 400;
  text-decoration: none;
  position: relative;
}
a.animated-link::before,
a.animated-link::after {
  content: "";
  position: absolute;
  height: 1px;
  width: 100%;
  bottom: -5px;
  left: 0;
  transform-origin: 0;
  transition: transform 0.2s ease-in-out;
}
a.animated-link::before {
  background: #ccc;
}
a.animated-link::after {
  transform: scaleX(0);
  background: #000;
  z-index: 2;
}
a.animated-link:hover::after {
  transform: scaleX(100%);
}
</style>
