<template>
    <div class="navBar">
        <img src="@/assets/logo-bookmark.svg" alt="logo de la marque">
        <nav>
            <a href="#feature">features</a>
            <a href="">pricing</a>
            <a href="">contact</a>
            <button class="btn">login</button>
        </nav>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>

    $SoftBlue: hsl(231, 69%, 60%);
    $SoftRed: hsl(0, 94%, 66%);
    $DarkBlue: hsl(229, 31%, 21%);
    $LightBlue: hsl(229, 8%, 60%);

    .navBar {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 125px;
        
        img {
            width: auto;
            height: 25px;
            margin-left: 10%;
        }
        nav {
            display: flex;
            align-items: center;
            margin-right: 11%;

            a, button {
                font-size: 12px;
                margin: 0 20px;
                text-transform: uppercase;
                text-decoration: none;
                letter-spacing: 1px;
            }
            a {
                color:  $DarkBlue;
            }
            button {
                background-color: $SoftRed;
            }
        }
    }
</style>