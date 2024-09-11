<script>
    import { introText } from "@/constants/index";
</script>

<template>
    <section class="intro" id="intro">
        <div class="intro__inner">
            <h2 class="intro__title">
                {{ introText.title }}
            </h2>
            <div class="intro__lines" aria-hidden="true">
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
            </div>
            <div class="intro__kv">
                <div class="intro__kv-text">
                    <div>{{ introText[0] }}</div>
                    <div>{{ introText[1] }}</div>
                    <div>{{ introText[2] }}</div>
                </div>
                <div class="intro__kv-img">
                    <img src="@/assets/img/about.jpg" alt="어바웃">
                </div>
            </div>
            <!-- <div class="intro__lines intro__lines--bottom" aria-hidden="true">
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
            </div> -->
        </div>
    </section>
</template>

<style lang="scss" scoped>
    .intro {
        height: 100vh;

        &__inner {
            width: 100%;
            height: 100%;
            display: flex;
            align-items: flex-start;
            justify-content: flex-end;
            flex-direction: column;
            padding: 16px;

            @media (max-width: 800px) {
                justify-content: center;
            }
        }

        &__title {
            font-size: 10vw;
            text-transform: uppercase;
            line-height: 1;
            font-weight: 800;
            white-space: nowrap;
            text-indent: -.5vw;
            letter-spacing: -.3vw;
        }

        &__kv {
            width: 100%;
            height: 40vh;
            background-color: var(--black);
            color: var(--white);
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            position: relative;

            &:hover {
                .intro__kv-text {
                    opacity: 0;
                }

                .intro__kv-img {
                    filter: grayscale(0);
                }
            }
        }

        &__kv-text {
            font-size: 3vw;
            line-height: 1;
            font-weight: 900;
            text-transform: uppercase;
            text-decoration: underline;
            text-align: center;
            position: relative;
            z-index: 100;
            transition: all .3s;
            cursor: all-scroll;

            @media (max-width: 800px) {
                font-size: 24px;
            }
        }

        &__kv-img {
            position: absolute;
            left: 0;
            right: 0;
            bottom: 0;
            top: 0;
            margin: auto;
            width: 30vh;
            height: 30vh;
            border-radius: 50%;
            overflow: hidden;
            filter: grayscale(100%);
            transition: all .3s;

            @media (max-width: 800px) {
                width: 20vh;
                height: 20vh;
            }
        }
    }
</style>