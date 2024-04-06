<template>
    <button class="btn" @click="handleClick">
      <slot></slot>
    </button>
  </template>
  
  <script>
  export default {
    methods: {
      handleClick() {
        this.$emit('click');
      }
    }
  }
  </script>
  
  <style>
  .btn {
    display: inline-block;
    margin-top: 1rem;
    padding: 0.8rem 3rem;
    background: var(--main-color);
    color: #fff;
    font-size: 1.7rem;
    border-radius: 2rem;
  }
  
  .btn:hover {
    background: #111;
    letter-spacing: 0.2rem;
  }
  </style>
  