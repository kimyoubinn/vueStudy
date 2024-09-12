<template>
    <section class="site" id="site">
        <div class="site__inner">
            <h2 class="site__title">
                site coding <em>나의 작업물</em>
            </h2>
            <div class="site__wrap">
                <article class="site__item s1">
                    <span class="site__item-number">1.</span>
                    <div class="site__item-text">
                        <div>Make</div>
                        <div>site compliant with</div>
                        <div>webstandard</div>
                    </div>
                    <h3 class="site__item-title">웹 표준을 준수한 사이트 제작</h3>
                    <div class="site__item-btn">
                        <a href="#">code</a>
                        <a href="#">view</a>
                    </div>
                    <div class="site__item-info">
                        <span>site coding</span>
                        <span>production period : two days</span>
                        <span>use stack : html5/css3, CSS Variable, Vite</span>
                    </div>
                </article>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    .site {
        &__inner {
            padding: 16px;

            .site__title {
                position: sticky;
                top: 70px;
                left: 0;
                width: 70%;
                height: 5vw;
                font-size: 4vw;
                font-weight: 900;
                line-height: 1.6;
                font-family: var(--mainKor-font);
                text-transform: uppercase;
                color: var(--black100);
                border-bottom: .4vw solid var(--black100);
                margin-bottom: 100px;

                @media (max-width: 800px){ 
                    width: 100%;
                    margin-bottom: 10vw;
                    font-size: 30px;
                    height: auto;
                    top: 68px;
                    z-index: 1000;
                    background-color: var(--mainBg-color);
                }

                em {
                    font-size: 1.25rem;
                    font-weight: 400;
                    line-height: 2;
                }
            }
        }

        &__item {
            height: 70vh;
            @include flex-center;
            flex-direction: column;
            position: sticky;
            left: 0;

            &:nth-child(1) {
                background-color: var(--subBg100);
                top: 180px;

                @media (max-width: 800px) {
                    top: 140px;
                }
            }

            &:nth-child(2) {
                background-color: var(--subBg200);
                top: 200px;

                @media (max-width: 800px) {
                    top: 160px;
                }
            }

            &:nth-child(3) {
                background-color: var(--subB300);
                top: 220px;

                @media (max-width: 800px) {
                    top: 180px;
                }
            }

            &:nth-child(4) {
                background-color: var(--subBg400);
                top: 240px;

                @media (max-width: 800px){ 
                    top: 200px;
                }
            }
        }

        &__item-number {
            font-size: 5vw;
            line-height: 1;
            font-weight: 900;
            font-family: var(--mainNum-font);
            position: absolute;
            left: 1vw;
            top: 1vw;

            @media (max-width: 800px){ 
                font-size: 80px;
                left: 20px;
                top: 20px;
            }
        }

        &__item-text {
            text-align: center;
            margin-bottom: 1rem;

            > div {
                font-size: 3vw;
                line-height: 1;
                font-weight: 900;
                text-transform: uppercase;
                text-decoration: underline;
                font-family: var(--mainEng-font);

                @media (max-width: 800px){ 
                    font-size: 26px;
                }
            }
        }

        &__item-title {
            font-family: var(--mainKor-font);
            margin-bottom: 1rem;
        }

        &__item-btn {
            text-decoration: underline;
            text-transform: uppercase;
            color: var(--black200);
            font-size: 1rem;
            transition: all 0.3s;
            margin: 0 2px;

            &:hover {
                color: var(--black);
            }
        }

        &__item-info {
            position: absolute;
            left: 0;
            bottom: 3%;
            width: 98%;
            margin-left: 1%;
            border-top: 1px solid var(--black);
            border-bottom: 1px solid var(--black);
            display: flex;
            justify-content: space-between;

            @media (max-width: 800px){ 
                flex-direction: column;
                width: 90%;
                margin-left: 5%;
                padding: 5px 0;
            }

            span {
                font-family: var(--mainKor-font);
                font-size: 12px;
                padding: 3px 0;
                text-transform: uppercase;
            }
        }
    }
</style>