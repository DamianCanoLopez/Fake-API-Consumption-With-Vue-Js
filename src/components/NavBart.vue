<script>
    export default {
        name: 'NavBart',
    }
</script>

<template>
    <div id="nav">
        <img src='../assets/img/logoP.svg' alt="logo">
        <div class="social-icon">
            <a href="https://www.linkedin.com/in/carlos-damian-cano-lopez-399812260/" style='textDecoration: none color: white'><img src="../assets/img/nav-icon1.svg" alt="Icon"/></a>
            <a href="https://github.com/DamianCanoLopez" style='textDecoration: none color: white'><img id='git' src="../assets/img/nav-icon4.svg" alt="Icon"/></a>
            <a href="https://damiancanolopez.vercel.app/" style='textDecoration: none color: white'><img src="../assets/img/nav-icon5.svg" alt="Icon"/></a>
        </div>
    </div>
</template>

<style>
#nav{
    background-color: black;
    width: 99vw;
    margin-left: -15.2%;
    display: flex;
    justify-content: space-between;
    padding: 3%;
}

.social-icon a {
    width: 42px;
    height: 42px;
    background: rgba(217, 217, 217, 0.1);
    display: inline-flex;
    border-radius: 50%;
    margin-right: 6px;
    align-items: center;
    justify-content: center;
    line-height: 1;
    border: 1px solid rgba(255, 255, 255, 0.5);

    
}

.social-icon #git{
    background-image: url(../assets/img/nav-icon4.svg);
    background-size: cover;
}
</style>