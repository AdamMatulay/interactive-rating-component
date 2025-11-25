<script>
    let { ratingResult } = $props();
</script>

<div class="confirm-message">
  <img src="./public/illustration-thank-you.svg" alt="" />
  <div class="rating-result">
    <p class="rating-result-text">You selected {ratingResult} out of 5</p>
  </div>
  <div class="confirm-text-content">
    <h1>Thank you!</h1>
    <p>
      We appreciate you taking the time to give a rating. If you ever need more
      support, don't hesitate to get in touch!
    </p>
  </div>
</div>

<style>
</style>