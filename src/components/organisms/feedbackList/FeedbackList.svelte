<script>
  // import {onMount, onDestroy} from 'svelte'
  import { FeedbackStore } from '../../../stores'
  import { fade, scale } from 'svelte/transition'
  import FeedbackItem from '../../molecules/feedbackItem/FeedbackItem.svelte'

  // The long way to retrieve/update FeedbackStore
  // let feedback = []
  // FeedbackStore.subscribe((data) => feedback = data)
  // onMount(() => {
  //   console.log('Mounted')
  // })
  // const unsubscribe = FeedbackStore.subscribe((data) => feedback = data)
  // onDestroy(() => {
  //   unsubscribe()
  // })
</script>

<!-- Instead we can add the '$FeedbackStore' below to retrieve/update FeedbackStore -->
{#each $FeedbackStore as fb (fb.id)}
<div in:scale="{{ duration: 200}}" out:fade="{{ duration: 200}}">
  <FeedbackItem item={fb} />
</div>
{/each}
