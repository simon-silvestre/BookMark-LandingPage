<template>
    <div class="navBar">
        <img src="@/assets/logo-bookmark.svg" alt="logo de la marque">
        <nav>
            <p>features</p>
            <p>pricing</p>
            <p>contact</p>
            <a href="" class="btn">login</a>
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
            margin-left: 11%;
        }
        nav {
            display: flex;
            align-items: center;
            margin-right: 11%;

            p, a {
                font-size: 13px;
                margin: 0 20px;
                text-transform: uppercase;
            }
            p {
                color:  $DarkBlue;
            }
            a {
                background-color: $SoftRed;
            }
        }
    }
</style>