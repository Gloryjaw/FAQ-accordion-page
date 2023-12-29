<script>
let width = window.innerWidth;
window.addEventListener("resize", ()=>{
    if(window.innerWidth >= 1050 || window.innerWidth< 1050){
        width = window.innerWidth
    }
})
</script>
{#if width < 1050}
<div class="mobile_container">
    <div class="mobile_img">
        <img src="./images/illustration-woman-online-mobile.svg" alt="illustration woman online">
    </div>
    <div class="mobile_shadow">
        <img src="./images/bg-pattern-mobile.svg" alt="background pattern">
    </div>

</div>
{:else}
<div class="desk_container">
    <div class="desk_img_container">
        <img class="desk_img" src="./images/illustration-woman-online-desktop.svg" alt="illustration woman online">
    </div>
    <img class="box" src="./images/illustration-box-desktop.svg" alt="background pattern">
</div>

{/if}
<style>
.desk_container{
    width: 50%;
    position: relative;

    align-self: center;

}
.desk_img_container{
    width: 100%;

    overflow: hidden;
    position: relative;

}
.box{
    position: absolute;
  top: 38%;
  width: 36%;
  left: -18%;
}
.desk_img{
    position: relative;
    left: -18%;
}
.mobile_container{

    position: relative;
    margin-bottom: 2em;
}
.mobile_img{
    position: absolute;
    z-index: 1;
    width: 80%;
   left: 50%;
   top: 0%;
   transform: translate(-50%, -60%);

}
.mobile_shadow>img{
    width: 100%;

}
.mobile_shadow{
    width: 80%;
    margin: auto;

}


</style>