<script>
    import ProgressBar from "./ProgressBar.svelte";

    const totalTime = 20;
    let secondsLeft = totalTime;
    function onClick() {
        let timer = setInterval(() => {
            secondsLeft -= 1;
            if (secondsLeft === 0) {
                clearInterval(timer);
            }
        }, 1000);
    }
</script>

<div bp="grid">
    <h2 bp="offset-5@md 4@md 12@sm">Seconds Left: {secondsLeft}</h2>
</div>

<ProgressBar progress="50" />

<div bp="grid">
    <button on:click={onClick} bp="offset-5@md 4@md 12@sm" class="start">Start</button>
</div>

<style>
    .start {
        background-color: green;
        width: 100%;
        margin: 10px 0;
    }
</style>
