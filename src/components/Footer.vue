<template>
    <div class="footer">
        <div class="navBar">
            <img src="@/assets/logo-bookmark-footer.svg" alt="logo de la marque">
            <nav>
                <a href="#feature">features</a>
                <a href="">pricing</a>
                <a href="#contact">contact</a>
            </nav>
        </div>
        <div class="social">
            <img src="@/assets/facebook.svg" alt="facebook">
            <img src="@/assets/twitter.svg" alt="twitter">
        </div>
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

    .footer {
        display: flex;
        align-items: center;
        justify-content: space-around;
        width: 100%;
        height: 75px;
        background-color: $DarkBlue;

        .navBar {
            display: flex;
            align-items: center;

            img {
                width: auto;
                height: 25px;
            }
            nav {
                margin-left: 40px;

                a {
                    font-size: 13px;
                    padding: 0 25px;
                    text-decoration: none;
                    color: #fff;
                    font-weight: 400;
                    opacity: .8;
                    text-transform: uppercase;
                    letter-spacing: 1px;
                    transition: ease .5s;

                    &:hover {
                        color: $SoftRed;
                    }
                }
            }
        }
        .social img {
            width: 25px;
            margin: 20px;
        }
    }
    @media screen and (max-width: 750px) {
        .footer {
            height: 330px;
            flex-direction: column;
            justify-content: center;

            .navBar {
                flex-direction: column;
                margin-bottom: 20px;

                img {
                    height: 30px;
                    margin-bottom: 40px;
                }

                nav {
                    display: flex;
                    flex-direction: column;
                    margin: 0;
                    text-align: center;

                    a {
                        font-size: 16px;
                        padding: 0 0 25px 0;
                    }
                }
            }
            .social img {
                margin: 0 20px;
            }
        }
    }
</style>