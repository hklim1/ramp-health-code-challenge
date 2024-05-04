<template>
    <div class="navbar">
        <div class="logo">
            <img src="../assets/jabberLogo.svg" height="150" width="150" />
        </div>
        <div class="links">
            <p>Link</p>
        </div>
    </div>
</template>

<style lang="scss">
.navbar {
    display: flex;
    padding-right: 30px;
    padding-left: 30px;
    justify-content: space-between;
    background-color: #ffffff;
}

.logo {
    display: flex;
    justify-content: flex-start;
}

.links {
    display: flex;
    justify-content: flex-end;
}
</style>