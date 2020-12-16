<template>
    <div class="faq">
        <div class="title">
            <h2>Frequently Asked Questions</h2>
            <p>Here are some of our FAQs. If you have any other questions you'd like answered please feel free to email us.</p>
        </div>
        <div class="questions">
            <details>
                <summary>What is Bookmark ?</summary>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, labore optio enim commodi laudantium hic, 
                        laboriosam amet architecto in, officiis doloribus nam vitae velit consectetur. Quo consequatur quia 
                        reprehenderit quidem!
                    </p>
            </details>
            <details>
                <summary>How can i request a new browser ?</summary>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, labore optio enim commodi laudantium hic, 
                        laboriosam amet architecto in, officiis doloribus nam vitae velit consectetur. Quo consequatur quia 
                        reprehenderit quidem!
                    </p>
            </details>
            <details>
                <summary>Is there a mobile app ?</summary>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, labore optio enim commodi laudantium hic, 
                        laboriosam amet architecto in, officiis doloribus nam vitae velit consectetur. Quo consequatur quia 
                        reprehenderit quidem!
                    </p>
            </details>
            <details>
                <summary>What about other Chromium browsers ?</summary>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, labore optio enim commodi laudantium hic, 
                        laboriosam amet architecto in, officiis doloribus nam vitae velit consectetur. Quo consequatur quia 
                        reprehenderit quidem!
                    </p>
            </details>
            <button class="btn">More Info</button>
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

    .faq {
        color: $LightBlue;
        margin-bottom: 150px;
        font-size: 18px;
        
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
        .questions {
            max-width: 540px;
            height: auto;
            padding: 0px 25px;
            margin: 0 auto;
            color: $DarkBlue;

            details {
                padding: 15px 0;
                border-bottom: 1px solid #e1e2e6;
                cursor: pointer;
                
                &:nth-child(1) {
                    border-top: 1px solid #e1e2e6;
                }
                &[open] summary::-webkit-details-marker {
                    transform: rotateZ(180deg);
                    color: $SoftRed;
                }

                summary {
                    outline: none;
                    opacity: .9;
                    display: flex;
                    align-items: center;
                    justify-content: space-between;
                    flex-direction: row-reverse;
                    transition: ease .5s;

                    &::-webkit-details-marker {
                        color: $SoftBlue;
                        width: 20px;
                        height: 20px;
                        transform: rotateZ(90deg);
                        margin-right: 15px;
                    }
                    &:hover {
                        color: $SoftRed;
                    }
                }
                p {
                    color: $LightBlue;
                    font-size: 16px;
                    padding: 30px 0 5px 0;
                    line-height: 30px;
                }
            }
            button {
                padding: 15px 30px;
                margin: 50px 0 0 calc(50% - 60px);
            }
        }
    }
    @media screen and (max-width: 499px) {
        .faq {
            font-size: 14px;

            .title {
                h2 {
                    font-size: 25px;
                }
                p {
                    padding: 0px 40px;
                }
            }
            .questions details {
                padding: 20px 0;
            }
        }
    }
</style>