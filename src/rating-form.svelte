<script>
  let { handleSubmit } = $props();
  let selected = $state(null);

  function internalSubmit(e) {
    e.preventDefault();
    if (handleSubmit) {
      handleSubmit(selected);
    }
  }
</script>

<form class="rating-form" onsubmit={internalSubmit}>
  <div class="star-wrapper">
    <img class="star-image" src="./public/icon-star.svg" alt="star" />
  </div>
  <div class="rating-text-content">
    <h1 class="rating-heading">How did we do?</h1>
    <p class="rating-text">
      Please let us know how we did with your support request. All feedback is
      appreciated to help us improve our offering!
    </p>
  </div>
  <div class="rating-buttons">
    <label class="rating-button"
      ><input
        type="radio"
        value="1"
        bind:group={selected}
        name="rating"
        required
      />1</label
    >
    <label class="rating-button"
      ><input
        type="radio"
        value="2"
        bind:group={selected}
        name="rating"
      />2</label
    >
    <label class="rating-button"
      ><input
        type="radio"
        value="3"
        bind:group={selected}
        name="rating"
      />3</label
    >
    <label class="rating-button"
      ><input
        type="radio"
        value="4"
        bind:group={selected}
        name="rating"
      />4</label
    >
    <label class="rating-button"
      ><input
        type="radio"
        value="5"
        bind:group={selected}
        name="rating"
      />5</label
    >
  </div>
  <button type="submit" id="submit">SUBMIT</button>
</form>

<style>
  .rating-form {
    max-width: 27em;
    min-height: 27em;
    background: linear-gradient(var(--Grey900), var(--Grey925));
    border-radius: 20px;
    padding: 2em;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .star-wrapper {
    background: var(--Grey700);
    width: 3em;
    height: 3em;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .star-image {
    width: 1.1em;
    height: 1.1em;
  }

  .rating-heading {
    font-size: 1.85rem;
    color: var(--White);
    margin-bottom: 0.5rem;
  }

  .rating-text {
    font-size: 1rem;
    color: var(--Grey500);
    line-height: 1.6;
    margin-bottom: -0.4em;
  }

  .rating-buttons {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }

  .rating-button input {
    position: absolute;
    opacity: 0;
    width: 1px;
    height: 1px;
    padding: 0;
    margin: -1px;
    overflow: hidden;
    clip: rect(0, 0, 0, 0);
    border: 0;
  }

  .rating-button {
    color: var(--Grey500);
    background: var(--Grey700);
    min-width: 3.4rem;
    min-height: 3.4rem;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 3px;
    font-size: 1rem;
    font-weight: bold;
    cursor: pointer;
    transition: 300ms;
  }

  #submit {
    color: var(--Grey900);
    font-weight: 700;
    letter-spacing: 0.1em;
    font-size: 1.1rem;
    background: var(--Orange500);
    border: none;
    outline: none;
    border-radius: 2em;
    padding: 0.95em 0.9em 0.9em 0.9em;
    cursor: pointer;
    transition: 300ms;
  }

  #submit:hover,
  #submit:focus,
  #submit:active {
    background: var(--White);
  }

  .rating-button:hover {
    background: var(--Orange500);
    color: var(--Grey900);
  }

  .rating-button:focus-within {
    background: var(--White);
    color: var(--Grey900);
  }

  @media (max-width: 26.5rem) {
    .rating-form {
      max-width: 22em;
      min-height: 24em;
      padding: 2rem 1.5rem;
    }

    .star-wrapper {
      width: 2.5em;
      height: 2.5em;
    }

    .star-image {
      width: 0.9em;
      height: 0.9em;
    }

    .rating-heading {
      font-size: 1.5rem;
    }

    .rating-text {
      font-size: 0.925rem;
    }

    .rating-button {
      min-width: 2.75rem;
      min-height: 2.75rem;
      font-size: 0.925rem;
    }

    #submit {
      font-size: 0.9rem;
      padding: 0.95em 0.9em 0.9em 0.9em;
    }
  }
</style>
