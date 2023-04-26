<script>
    export let answerText
    export let checkAnswerHandler
</script>



<button class="btn btn-outline-primary" on:click={() => checkAnswerHandler(answerText)} >
    {answerText}
</button>