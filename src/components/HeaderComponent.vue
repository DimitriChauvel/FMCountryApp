<template>
  <header>
    <span class="title">Where in the world?</span>
    <button>
      <ion-icon name="moon-outline"></ion-icon>
      <span>Dark Mode</span>
    </button>
  </header>
</template>

<style scoped>
  header {
    padding: 1.5em 5em;

    display: flex;
    align-items: center;
    justify-content: space-between;

    white-space: nowrap;

    box-shadow: var(--component-shadow);
    background-color: var(--light-component);
  }
  .title {
    font-weight: 800;
    font-size: 1.5em;
  }

  button {
    background: unset;
    border: unset;
    border-radius: unset;
    outline: unset;
    
    display: flex;
    gap: 10px;
    align-items: center;

    font-size: 1em;
    font-weight: 600;
  }

  @media (max-width: 550px) {
    header {
      padding: 1.5em 1em;
    }

    .title {
      font-size: 1em;
    }
  }
</style>