<template>
    <header>
        <div class="title">
            <h1>A Simple Bookmark Manager</h1>
            <p>A clean and simple interface to organize your favourite websites. Open a new browser tab and see your sites load instantly. Try it for free.</p>
            <button class="btn">Get it on Chrome</button>
            <button class="btn">Get it on Firefox</button>
        </div>
        <div class="ContainerImg">
            <img src="" alt="">
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
        flex-wrap: wrap;

        .title {
            margin-left: 11%;
            width: 30%;

            h1 {
                color: $DarkBlue;
                font-weight: 500;
                font-size: 40px;
                margin-bottom: 30px;
            }
            p {
                color: $LightBlue;
                line-height: 25px;
            }
            button {
                border: none;
                padding: 15px 22px;
                margin-top: 40px;
                box-shadow: none;
                font-weight: 600;
                &:nth-last-child(1) {
                    margin-left: 10px;
                    background-color: #f7f7f7;
                    color: $LightBlue;
                    box-shadow: 0px 10px 27px -12px rgba(128,128,128,1);
                }
            }
        }
    }
</style>