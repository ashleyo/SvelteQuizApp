<script>

    export let questionText

</script>

<style>
    .Question {
        color:darkcyan;
        background-color: aqua;
        padding: 0.25em;
        border-radius: 5px;
        width:fit-content;
    }
</style>

<h2 class="alert alert-secondary w-75">
    {@html questionText}
</h2>