<script>
    let { onFormSubmit } = $props();
    let selected = $state(null);

    function internalSubmit(e) {
        e.preventDefault();
        if (onFormSubmit) {
            onFormSubmit(selected);
        }
    }
</script>

<form class="rating-form" onsubmit={internalSubmit}>
  <div>
    <img src="./public/icon-star.svg" alt="star" />
  </div>
  <div class="rating-text-content">
    <h1>How did we do?</h1>
    <p>
      Please let us know how we did with your support request. All feedback is
      appreciated to help us improve our offering!
    </p>
  </div>
  <div class="rating-buttons">
    <label><input type="radio" name="rating" value="1" required bind:group={selected} /> 1</label>
    <label><input type="radio" name="rating" value="2" bind:group={selected} /> 2</label>
    <label><input type="radio" name="rating" value="3" bind:group={selected} /> 3</label>
    <label><input type="radio" name="rating" value="4" bind:group={selected} /> 4</label>
    <label><input type="radio" name="rating" value="5" bind:group={selected} /> 5</label>
  </div>
  <button type="submit" id="submit">SUBMIT</button>
</form>

<style>
</style>