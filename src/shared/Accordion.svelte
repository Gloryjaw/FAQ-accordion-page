<script>
    export let acc_data;
    let show = false;
    import {slide} from "svelte/transition"
</script>

<div class="container" >
    <div  class="question" on:click = {()=>{show = !show}} on:keypress = {()=>{show = !show}}>
        <p class="question_text" class:dark = {show} >{acc_data.question}</p>
        <button>
            <img src="./images/icon-arrow-down.svg" alt="arrow down" class:rotate = {show}>
        </button>
    </div>

    {#if show}
    <div class="answer" in:slide = {{duration:500, axis:"y"}} out:slide = {{duration:500, axis:"y"}}>
        <p>{acc_data.answer}</p>
    </div>
    {/if}
</div>


<style>
.dark{
    color: var(--vd-desat-blue);
    font-weight: 700;
}
.question, .answer{
    font-size: 0.8rem;
}
.question{
    display: flex;
    color: var(--vd-gray-blue);
    justify-content: space-between;
}
img{
    transition: 0.5s transform;
}
button{
    background-color: white;
    padding: 0;
    align-self: center;
    border: none;
    padding: 0.1em;
    
}
.question_text:hover{
    cursor: pointer;
    color: var(--soft-red);
}
.rotate{
    transform: rotate(180deg);
}
.container{
    border-bottom: 2px solid var(--divider);
    padding: 1em 0;
}
.answer{
    padding-top: 1em;
    color: var(--d-gray-blue);
}
</style>