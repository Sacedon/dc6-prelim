<template>
    <div class="custom-card m-4 transition-transform transform hover:-translate-y-1 hover:shadow-lg">
      <div class="card-content">
        <div class="icon">
          <i class="fa-solid fa-user-tie text-4xl mb-2"></i>
        </div>
        <h5 class="card-title text-xl font-semibold">
          {{ client.first_name }} {{ client.last_name }}
        </h5>
        <div class="card-details mt-2">
          <p class="card-text">{{ client.address }}</p>
          <p class="card-text">{{ client.phone }}</p>
        </div>
        <span class="card-level mt-2">Level {{ client.level }}</span>
      </div>
    </div>
  </template>

  <style scoped>
  .custom-card {
    width: 350px;
    background-color: rgb(101, 159, 224);
    border: 1px solid #e2e8f0;
    border-radius: 0.5rem;
    margin: 0.5rem;
    cursor: pointer;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    transition: transform 0.2s, box-shadow 0.2s;
  }

  .custom-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }

  .card-content {
    padding: 1rem;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    justify-content: center; /* Center content vertically */
    align-items: center; /* Center content horizontally */
  }

  .card-title {
    font-size: 1.25rem;
    font-weight: bold;
    color: #222020;
  }

  .icon {
    color: #222020;
  }

  .card-details {
    color: #352020;
  }

  .card-text {
    margin-bottom: 0.25rem;
  }

  .card-level {
    font-size: 0.75rem;
    background-color: #48bb78;
    padding: 0.25rem 0.5rem;
    border-radius: 0.25rem;
    color: white;
    align-self: flex-start;
  }
  </style>

  <script setup>
  import { defineProps } from 'vue';

  const props = defineProps({
    client: Object,
  });
  </script>
