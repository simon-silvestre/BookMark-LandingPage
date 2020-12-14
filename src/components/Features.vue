<template>
    <div class="feature">
        <div class="title">
            <h2>Features</h2>
            <p>
                Our aim is to make it quick and easy for you to access your favorite websites. 
                Your bookmarks sync between your devices so you can access them on the go.
            </p>
        </div>
        <div class="featureMenu">
            <button :class="{ active : index == 0 }" @click.prevent="index = 0">Simple Bookmarking</button>
            <button :class="{ active : index == 1 }" @click.prevent="index = 1">Speedy Searching</button>
            <button :class="{ active : index == 2 }" @click.prevent="index = 2">Easy Sharing</button>
        </div>
        <div class="featureSlide">
            <div class="featureImg">
                <span class="featureImgOvale"></span>
                <img :src="features[index].img" alt="illustration">
            </div>
            <div class="featureDescription">
                <h2>{{ features[index].title }}</h2>
                <p>{{ features[index].text }}</p>
                <button class="btn featureBtn">More Info</button>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            index: 0,
            features: [
                {
                    img: '/img/illustration-features-tab-1.25a23733.svg',
                    title: 'Bookmark in one click',
                    text: 'Organize your bookmarks however you like. Our simple drag-and-drop interface gives you complete control over how you manage your favourite sites.'
                },
                {
                    img: '/img/illustration-features-tab-2.25a23733.svg',
                    title: 'Bookmark in one click',
                    text: 'Organize your bookmarks however you like. Our simple drag-and-drop interface gives you complete control over how you manage your favourite sites.'
                },
                {
                    img: '/img/illustration-features-tab-1.25a23733.svg',
                    title: 'Bookmark in one click',
                    text: 'Organize your bookmarks however you like. Our simple drag-and-drop interface gives you complete control over how you manage your favourite sites.'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

    $SoftBlue: hsl(231, 69%, 60%);
    $SoftRed: hsl(0, 94%, 66%);
    $DarkBlue: hsl(229, 31%, 21%);
    $LightBlue: hsl(229, 8%, 60%);

    .feature {
        width: 100%;
        height: auto;
        margin-top: 100px;
        margin-bottom: 150px;
        color: $LightBlue;

        h2 {
            color: $DarkBlue;
            font-size: 30px;
            font-weight: 500;
            margin-bottom: 25px;
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
        .featureMenu {
            max-width: 640px;
            margin: 0 auto;
            border-bottom: 1px solid #e1e2e6;

            button {
                color: rgba(0, 0, 0, 0.5);
                width: 33%;
                height: 75px;
                background-color: transparent;
                border: none;
                font-size: 16px;
                outline: none;
                cursor: pointer;

                &.active {
                    border-bottom: 5px solid $SoftRed;
                    color: rgba(0, 0, 0, 0.8);
                }
            }
        }
        .featureSlide {
            display: flex;
            align-items: center;

            .featureImg {
                margin-top: 70px;
                width: 700px;
                height: fit-content;
                position: relative;

                img {
                    width: 77%;
                    margin-left: 23%;
                }
                .featureImgOvale {
                    position: absolute;
                    width: 90%;
                    height: 100%;
                    top: 25%;
                    left: 0;
                    background-color: $SoftBlue;
                    border-radius: 0px 200px 200px 0px;
                    z-index: -1;
                }
            }
            .featureDescription {
                width: 475px;
                margin: 70px 5% 0 8%;
                padding: 0 15px;

                .featureBtn {
                    margin-top: 30px;
                    padding: 15px 30px;
                }
            }
        }
    }
    @media screen and (min-width: 1441px) {
        .feature .featureSlide .featureDescription {
            width: 32%;
        }
    }
      @media screen and (max-width: 1200px) {
        .feature {
            .featureSlide .featureDescription {
                margin: 50px 5% 0 8%;
           
            }
            .featureImg {
                width: 500px;
            }   
        } 
    }
    @media screen and (max-width: 980px) {
        .feature {
            margin-top: 150px;
        
            .featureSlide {
                flex-direction: column;

                .featureDescription {
                    width: 90%;
                    text-align: center;
                    margin: 150px 0 0 0;
                }
                .featureImg {
                    width: 700px;
                    align-self: flex-start;

                    img {
                        margin-left: 7vw;
                    }
                    .featureImgOvale {
                        width: 75%;
                    }
                }
            }
        }
    }
    @media screen and (max-width: 700px) {
        .feature .featureMenu {
            width: 80%;
            display: flex;
            flex-direction: column;
            align-items: center;
            border-top: 1px solid #e1e2e6;

            button {
                width: 100%;
                height: 60px;
                border-top: 1px solid #e1e2e6;
                border-bottom: 1px solid #e1e2e6;

                &:nth-child(1) {
                    border-top: none;
                }
                &.active {
                    width: fit-content;
                    border-top: none;
                    border-width: 3px;
                }
            }
        }
        .feature .featureSlide .featureImg {
             width: 100%;
            align-self: flex-start;

            img {
                width: 85%
            }
        }
    }
    @media screen and (max-width: 499px) {
        .feature {
            h2 {
                font-size: 25px;
            }
            p {
                font-size: 14px;
            }
            .title p {
                padding: 0px 40px;
            }
            .featureSlide .featureDescription {
                padding: 0px 21px;
            }
        }
    }
</style>