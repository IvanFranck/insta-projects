<template>
    <div class="container">
        <div class="illustration__container">
        </div>
        <div class="content">
            <h1>Stay updated!</h1>
            <p>
                Join 60,000+ product managers receiving monthly updates on:
            </p>

            <ul>
                <li>
                    Product discovery and building what matters
                </li>
                <li>
                    <span>Measuring to ensure updates are a success</span>
                </li>
                <li>
                    <span>And much more!</span>
                </li>
            </ul>
        </div>
        <div class="form__container">
            <form>
                <div class="form__group">
                    <label for="email">Email adddres</label>
                    <input type="email" name="email" id="email" placeholder="email@company.com">
                </div>
                <button type="submit">Subscribe to monthly newsletter</button>
            </form>
            
        </div>
    </div>

</template>

<style lang="scss" scoped>
    .container{
        width: 100%;
        min-height: 100vh;
        display: flex;
        flex-direction: column;
        gap: 32px;

        .illustration__container{
            width: 100%;
            background-image: url('/src/assets/img/illustration-sign-up-mobile.svg');
            height: 300px;
            background-position: center;
            background-size: cover;
            border-bottom-left-radius: 16px;
            border-bottom-right-radius: 16px;
        }

        .content{
            padding: 0 12px;
            display: flex;
            flex-direction: column;
            align-items: start;
            gap: 16px;

            h1{
                font-weight: 700;
                color: var(--text-heading);
            }
            p{
                line-height: 1.3;
            }
            ul{
                list-style-image: url('/src/assets/img/icon-list.svg');
                list-style-position: initial;
            }
        }


    }
</style>