<script>
    export let progress;
</script>

<style>
    .progress-container {
        margin: 20px 0;
        border: solid 1px #cbc0c0;
        
    }

    .progressbar {
        height: 30px;
        background-color: rgb(77, 199, 55);
    }
</style>

<div bp="grid">
    <div class="progress-container" bp="offset-5@md 4@md 12@sm">
        <div class="progressbar" style="width: {progress}%">
            <span class="sr-only">%</span>
        </div>
    </div>
</div>