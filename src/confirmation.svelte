<script>
  let { ratingResult } = $props();
</script>

<div class="confirm-message">
  <img src="./public/illustration-thank-you.svg" alt="" />
  <div class="rating-result">
    <p class="rating-result-text">You selected {ratingResult} out of 5</p>
  </div>
  <div class="confirm-text-content">
    <h1 class="confirm-heading">Thank you!</h1>
    <p class="confirm-text">
      We appreciate you taking the time to give a rating. If you ever need more
      support, don't hesitate to get in touch!
    </p>
  </div>
</div>

<style>
  .confirm-message {
    max-width: 27em;
    min-height: 27em;
    background: linear-gradient(var(--Grey900), var(--Grey925));
    border-radius: 20px;
    padding: 2.2em;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 2em;
  }

  .confirm-message img {
    max-width: 10.5em;
  }

  .rating-result {
    background: var(--Grey700);
    border-radius: 2em;
    padding: 0.5rem 1.25rem;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .rating-result-text {
    color: var(--Orange400);
    font-size: 1rem;
    margin-top: 3px;
  }

  .confirm-heading {
    font-size: 1.85rem;
    color: var(--White);
    margin: 0.4rem 0 0.6rem 0;
    text-align: center;
  }

  .confirm-text {
    font-size: 1rem;
    color: var(--Grey500);
    line-height: 1.6;
    text-align: center;
  }

  @media (max-width: 26.5rem) {
    .confirm-message {
      max-width: 22em;
      min-height: 24em;
      padding: 2rem 1.5rem;
    }

    .confirm-message img {
      max-width: 10em;
    }

    .rating-result {
      padding: 0.3rem 0.75rem;
    }

    .rating-result-text {
      font-size: 0.925rem;
    }

    .confirm-heading {
      font-size: 1.5rem;
      margin: 0rem 0 0.6rem 0;
    }

    .confirm-text {
      font-size: 0.925rem;
    }
  }
</style>
