<script setup>
    import { skillText } from "@/constants/index";
</script>

<template>
    <section class="skill" id="skill">
        <div class="skill__inner">
            <h2 class="skill__title">
                challengh <em>나의 도전</em>
            </h2>
            <ul class="skill__desc">
                <li 
                    v-for="(item, key) in skillText"
                    :key="key">
                    <span>{{ key + 1 }}</span>
                    <h3>{{ item.title }}</h3>
                    <p>{{ item.desc }}</p>
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    .skill {
        &__inner {
            padding: 16px;
            display: flex;
            justify-content: space-between;

            @media (max-width: 800px) {
                flex-direction: column;
            }
        }

        &__title {
            position: sticky;
            top: 70px;
            left: 0;
            width: 48%;
            height: 5vw;
            font-size: 4vw;
            font-weight: 900;
            line-height: 1.6;
            font-family: var(--mainKor-font);
            text-transform: uppercase;
            color: var(--black100);
            border-bottom: .4vw solid var(--black100);

            @media (max-width: 800px) {
                width: 100%;
                margin-bottom: 10vw;
                font-size: 30px;
                height: auto;
                top: 68px;
                background-color: var(--mainBg-color);
            }
        }
        
        em {
            font-size: 1.25rem;
            font-weight: 400;
            line-height: 2;
        }

        .skill__desc {
            width: 50%;

            @media (max-width: 800px) {
                width: 100%;
            }

            span {
                font-size: 5vw;
                line-height: 1;
                font-weight: 900;
                line-height: 1.3;
                font-family: var(--mainNum-font);

                @media (max-width: 800px) {
                    font-size: 20vw;
                }
            }

            h3 {
                font-size: 1.4rem;
                text-decoration: underline;
                text-underline-position: under;
                margin-bottom: 1vw;
            }

            p {
                margin-bottom: 30vw;
                font-size: 1.1rem;
            }
        }
    }
</style>