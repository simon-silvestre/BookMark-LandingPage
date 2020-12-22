<template>
    <header>
        <div class="title" data-aos="fade-down" data-aos-duration="1000">
            <h1>A Simple Bookmark Manager</h1>
            <p>A clean and simple interface to organize your favourite websites. Open a new browser tab and see your sites load instantly. Try it for free.</p>
            <button class="btn">Get it on Chrome</button>
            <button class="btn">Get it on Firefox</button>
        </div>
        <div class="ContainerImg" data-aos="fade-left" data-aos-duration="1000">
            <span class="containerImg__ovale"></span>
            <img src="@/assets/illustration-hero.svg" alt="">
        </div>
    </header>
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
    
    header {
        display: flex;
        justify-content: space-between;
        margin-top: 50px;

        .title {
            width: 480px;
            margin: 70px 0  0 10%;

            h1 {
                color: $DarkBlue;
                font-weight: 500;
                font-size: 45px;
                margin-bottom: 30px;
            }
            p {
                color: $LightBlue;
                line-height: 25px;
                font-size: 18px;
            }
            button {
                padding: 15px 22px;
                margin-top: 40px;
                box-shadow: none;
                font-weight: 600;

                &:hover {
                    background-color: #fff!important;
                    border: 2px solid $SoftBlue;
                    color: $SoftBlue;
                }
                &:nth-last-child(1) {
                    margin-left: 10px;
                    background-color: #f7f7f7;
                    color: $LightBlue;
                    box-shadow: 0px 10px 27px -12px rgba(128,128,128,1);

                    &:hover {
                        border: 2px solid $DarkBlue;
                        color: $DarkBlue;
                        box-shadow: none;
                    }
                }
            }
        }
        .ContainerImg {
            max-width: 700px;
            height: fit-content;
            position: relative;
            
            img {
                width: 100%;
            }
            .containerImg__ovale {
                position: absolute;
                width: 72%;
                height: 70%;
                top: 32%;
                right: 0;
                background-color: $SoftBlue;
                border-radius: 200px 0px 0px 200px;
                z-index: -1;
            }
        }
    }
    @media screen and (min-width: 1441px) {
        header {
            .title {
                width: 32%;
                margin: 70px 0 0 15%;
            }
        }
    }
    @media screen and (max-width: 1200px) {

        header {
            .title {
                margin: 50px 0 0 5%;
            }
            .ContainerImg {
                max-width: 500px;
            }
        }
    }
    @media screen and (max-width: 980px) {
        
        header {
            flex-direction: column-reverse;
            align-items: center;

            .title {
                width: 90%;
                text-align: center;
                margin: 50px 0 0 0;
            }
            .ContainerImg {
                max-width: 700px;
                align-self: flex-end;
            }
        }
    }
    @media screen and (max-width: 499px) {
        header {
            .title {

                h1 {
                    font-size: 30px;
                }
                p {
                    font-size: 14px;
                    padding: 0 8%;
                }
            }
        }
    }
</style>