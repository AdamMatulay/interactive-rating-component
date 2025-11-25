<main>
  <form class="rating-form">
    <div>
      <img src="./public/icon-star.svg" alt="star">
    </div>
    <div class="rating-text-content">
      <h1>How did we do?</h1>
      <p>
        Please let us know how we did with your support request. All feedback is
        appreciated to help us improve our offering!
      </p>
    </div>
    <div class="rating-buttons">
      <label><input type="radio" name="rating" value="1" required /> 1</label>
      <label><input type="radio" name="rating" value="2" /> 2</label>
      <label><input type="radio" name="rating" value="3" /> 3</label>
      <label><input type="radio" name="rating" value="4" /> 4</label>
      <label><input type="radio" name="rating" value="5" /> 5</label>
    </div>
    <button type="submit" id="submit">SUBMIT</button>
  </form>

  <div class="confirm-message">
    <img src="./public/illustration-thank-you.svg" alt="">
    <div class="rating-result">
        <p class="rating-result-text"></p>
    </div>
    <div class="confirm-text-content">
        <h1>Thank you!</h1>
        <p>We appreciate you taking the time to give a rating. If you ever need more support, don't hesitate to get in touch!</p>
    </div>
  </div>
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
    --Orange500: hsl(25, 97%, 53%);
    --White: hsl(0, 100%, 100%);
    --Grey500: hsl(217, 12%, 63%);
    --Grey900: hsl(213, 19%, 18%);
    --Grey950: hsl(216, 12%, 8%);
  }

  :global(body) {
    font-family: "Overpass", sans-serif;
  }

  
</style>
