<template>
    <div id="contact">
        <p>35,000+ already joined</p>
        <h2>Stay up-to-date with what we're doing</h2>
        <form @submit.prevent>
            <input type="email" placeholder="Enter your email adress">
            <button class="btn">Contact Us</button>
        </form>
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

    #contact {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        width: 100%;
        height: 300px;
        background-color: $SoftBlue;
        color: #fff;

        h2 {
            max-width: 400px;
            text-align: center;
            font-weight: 500;
            margin-bottom: 25px;
            font-size: 30px;
        }
        p {
            line-height: 28px;
            font-size: 18px;

            &:nth-child(1) {
                font-size: 10px;
                text-transform: uppercase;
                letter-spacing: 8px;
                margin-bottom: 25px;
            }
        }
        input, button {
            padding: 12px 25px;
            border-radius: 5px;
            border: none;
            outline: none;
        }
        input {
            width: 250px;
        }
        button {
            background-color: $SoftRed;
            margin-left: 15px;
            box-shadow: none;
        }
    }
    @media screen and (max-width: 435px) {
        #contact {
            h2 {
                max-width: 375px;
                font-size: 25px;
                padding: 0 10px;
            }
            p:nth-child(1) {
                margin-bottom: 10px;
                font-size: 9px;
            }
            form {
                width: 85%;
                display: flex;
                flex-direction: column;
                justify-content: center;

                input {
                    width: 100%;
                }
                button {
                     margin: 15px 0 0 0;
                }
            }
        }
    }
</style>