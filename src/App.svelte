<script>
  import RatingForm from "./rating-form.svelte";
  import Confirmation from "./confirmation.svelte";

  let formState = $state(false);
  let ratingResult = $state(null);

  function handleSubmit(selected) {
    ratingResult = selected;
    formState = true;
  }
</script>

<main>
  {#if formState}
    <Confirmation {ratingResult} />
  {:else}
    <RatingForm {handleSubmit} />
  {/if}
</main>

<style>
  :global(*),
  :global(body) {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  :root {
    font-size: 15px;
    --Orange400: hsl(25, 80%, 52%);
    --Orange500: hsl(25, 97%, 53%);
    --White: hsl(0, 100%, 100%);
    --Grey500: hsl(217, 12%, 63%);
    --Grey700: hsl(212, 14%, 21%);
    --Grey900: hsl(213, 19%, 18%);
    --Grey925: hsl(213, 13%, 13%);
    --Grey950: hsl(216, 12%, 8%);
  }

  :global(body) {
    font-family: "Overpass", sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100dvh;
    background: var(--Grey950);
  }
</style>
