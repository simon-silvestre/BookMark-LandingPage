<template>
    <div class="extensions">
        <div class="title">
            <h2>Download the extension</h2>
            <p>We've got more browsers in the pipeline. please do let us know if you've got a favourite you'd like us to prioritize.</p>
        </div>
        <div class="cardsContainer">
            <div class="card">
                <div class="imgContainer">
                    <img src="@/assets/chrome.svg" alt="">
                </div>
                <h3>Add to Chrome</h3>
                <p>Minimum version 62</p>
                <hr class="cardSeparateur">
                <button class="btn">Add & install Extension</button>
            </div>
            <div class="card">
                <div class="imgContainer">
                    <img src="@/assets/firefox.svg" alt="">
                </div>
                <h3>Add to Firefox</h3>
                <p>Minimum version 55</p>
                <hr class="cardSeparateur">
                <button class="btn">Add & install Extension</button>
            </div>
            <div class="card">
                <div class="imgContainer">
                    <img src="@/assets/opera.svg" alt="">
                </div> 
                <h3>Add to Opera</h3>
                <p>Minimum version 46</p>
                <hr class="cardSeparateur">
                <button class="btn">Add & install Extension</button>
            </div>
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

    .extensions {
        color: $LightBlue;
        margin-bottom: 150px;

        h2, h3 {
            color: $DarkBlue;
            font-weight: 500;
            margin-bottom: 25px;
        }
        h2 {
            font-size: 30px;
        }
        p {
            line-height: 28px;
            font-size: 18px;
        }
        .title {
            max-width: 550px;
            margin: 0 auto;
            text-align: center;
            margin-bottom: 30px;

            p {
                padding: 0 15px;
            }
        }
        .cardsContainer
        {
            margin-top: 50px;
            width: 100%;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            
            .card {
                position: relative;
                overflow: hidden;
                margin: 0 20px;
                width: 280px;
                height: 360px;
                border-radius: 15px;
                box-shadow: 0 15px 40px rgba(154,160,185,.05), 0 5px 10px hsla(231, 69%, 60%, .2);

                &:nth-child(2) {
                    margin-top: 40px;
                }
                &:nth-child(3) {
                    margin-top: 80px;;
                }
                .imgContainer, h3, p, .cardSeparateur, button {
                    position: absolute;
                }
                .imgContainer {
                    width: 100px;
                    height: 100px;
                    top: 50px;
                    left: calc(50% - 50px);
                }
                h3, p {
                    width: 100%;
                    display: flex;
                    justify-content: center;
                }
                h3 {
                    font-size: 20px;
                    top: 185px;
                }
                p {
                    top: 210px;
                    font-size: 15px;
                }
                .cardSeparateur {
                    width: 100%;
                    top: 250px;
                    border: none;

                    &::after {
                        content: "..........................";
                        letter-spacing: 10px;
                        font-size: 24px; 
                        color: $LightBlue; 
                        opacity: .5;
                    }
                }
                button {
                    bottom: 20px;
                    left: calc(50% - 104.4px);
                    padding: 15px 30px;
                    box-shadow: none;
                }
            }
        }
    }
    @media screen and (max-width: 974px) {
        .extensions .cardsContainer .card:nth-child(3) {
            margin-top: 40px;
        }
    }
    @media screen and (max-width: 499px) {
        .extensions {
            .title {
                h2 {
                    font-size: 25px;
                }
                p {
                    font-size: 14px;
                    padding: 0px 40px;
                }
            }
        }
    }
</style>