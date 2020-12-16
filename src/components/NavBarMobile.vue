<template>
    <div class="navBarMobile">
        <div class="navContainer" :class="{'open':showNav}">
            <div class="navHeader">
                <img src="@/assets/logo-bookmark-mobile.svg" alt="logo de la marque">
                <h2 @click="showNav = !showNav">X</h2>
            </div>
            <nav>
                <a href="#feature">features</a>
                <a href="">pricing</a>
                <a href="#contact">contact</a>
                <button class="btn">login</button>
            </nav>
            <div class="social">
                <img src="@/assets/facebook.svg" alt="facebook">
                <img src="@/assets/twitter.svg" alt="twitter">
            </div>
        </div>
        <div class="navBar">
            <img v-show="!showNav" src="@/assets/logo-bookmark.svg" alt="logo de la marque">
            <img v-show="!showNav" src="@/assets/menu_icon.svg" alt="icon menu hamburger" @click="showNav = !showNav">
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            showNav: false
        }
    }
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
            
            &:nth-child(1) {
                margin-left: 10%;
                fill: #fff;
            }
            &:nth-child(2) {
                margin-right: 10%;
                cursor: pointer;
            }
        }
    }
    .navBarMobile .navContainer {
        display: none;
    }
    .navBarMobile .navContainer.open {
        display: flex;
        position: fixed;
        width: 100%;
        height: 100vh;
        flex-direction: column;
        align-items: center;
        background-color: hsla(229, 31%, 21%, 0.904);
        z-index: 100;
        color: #fff;

        .navHeader {
            width: 80%;
            display: flex;
            justify-content: space-between;
            padding: 50px 0 50px 0;

            img {
                height: 30px;
            }
            h2 {
                cursor: pointer;
              
            }
        }
        .navHeader, a {
            border-bottom: 1px solid $LightBlue;
        }
        nav {
            display: flex;
            flex-direction: column;
            width: 80%;
        }

        a, button {
            font-size: 22px;
            text-transform: uppercase;
            text-decoration: none;
            letter-spacing: 2.5px;
            color: #fff;
        }
        a {
            padding: 25px 0 25px 0;
            text-align: center;
        }
        button {
            margin-top: 25px;
            background-color: transparent;
            border: 3px solid #fff;
            box-shadow: none;
            outline: none;
            cursor: pointer;
        }
        .social {
            position: absolute;
            bottom: 5vw;

            img {
                width: 30px;
                margin: 25px;
            }
        }
    }
</style>