<script>
    export let points

</script>

<style>
    .Points {
        position: absolute;
        right: 5px;
        top: 5px;
        color: green;
        background-color: palegreen;
        border: 1px solid darkgreen;
        border-radius: 5px;
        padding: 1em;
        font-weight: bold;
        font-size:x-large;
    }
</style>

<button class="btn btn-success position-absolute top-00 end-0">
    Score <span class="badge text-bg-warning">{points}</span>
</button>