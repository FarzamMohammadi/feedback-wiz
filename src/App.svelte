<script>
  import FeedbackList from './components/organisms/feedbackList/FeedbackList.svelte';
  import FeedbackStats from './components/molecules/feedbackStats/FeedbackStats.svelte';
  import FeedbackForm from './components/organisms/feedbackForm/FeedbackForm.svelte';
  // Updating Feedback array without using store
  // const deleteFeedback = (e) => {
  //   const itemId = e.detail
  //   feedback = feedback.filter((item) => item.id != itemId)
  // }

  // const addFeedback = (e) => {
  //   const newFeedback = e.detail
  //   feedback = [newFeedback, ...feedback]
  // }

  // <FeedbackForm on:add-new-feedback={addFeedback}/>
  // <FeedbackStats {count} {average}/>
  // <FeedbackList on:delete-feedback={deleteFeedback}/>
</script>

<main class="container">
  <FeedbackForm/>
  <FeedbackStats/>
  <FeedbackList/>
</main>

<style>
</style>
