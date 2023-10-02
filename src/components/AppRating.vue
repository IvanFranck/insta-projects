<script setup>
import {ref} from 'vue'

const emits = defineEmits(['submit'])
const selectedNote = ref()

const ratingOptions = [1,2,3,4,5]
</script>
<template>
    <div class="card__container">
        <div class=" card__header">
            <div class="icon__container">
                <svg width="17" height="16" xmlns="http://www.w3.org/2000/svg"><path d="m9.067.43 1.99 4.031c.112.228.33.386.58.422l4.45.647a.772.772 0 0 1 .427 1.316l-3.22 3.138a.773.773 0 0 0-.222.683l.76 4.431a.772.772 0 0 1-1.12.813l-3.98-2.092a.773.773 0 0 0-.718 0l-3.98 2.092a.772.772 0 0 1-1.119-.813l.76-4.431a.77.77 0 0 0-.222-.683L.233 6.846A.772.772 0 0 1 .661 5.53l4.449-.647a.772.772 0 0 0 .58-.422L7.68.43a.774.774 0 0 1 1.387 0Z" fill="#FC7614"/></svg>
            </div>
            <h1>How did we do?</h1>
        </div>
        <div class="card__body">
            <p>
                Please let us know how we did with your support request. All feedback is appreciated to help us improve our offering!

            </p>
            <ul class="rating__options">
                <li 
                    v-for="item in ratingOptions"
                    :key="item"
                    :class="{'item--selected': item === selectedNote}"
                    @click="selectedNote = item"
                    class="item"
                >
                    {{ item }}
                </li>
            </ul>
        </div>

        <div class="card__cta">
            <button @click="emits('submit', {status: false, selectedNote})">SUBMIT</button>
        </div>
    </div>
</template>

<style lang="scss" scoped>

.card__container{
    width: 100%;
    padding: 32px 24px;
    background-color: var(--color-dark-blue);
    border-radius: 12px;
    box-shadow: var(--black-shadow);
}

.card__header{
    width: 100%;
    display: block;

    .icon__container{
        width: 40px;
        height: 40px;
        border-radius: 50%;
        background-color: var(--color-dark-blue-2);
        display: grid;
        align-content: center;
        justify-items: center;
    }

    h1{
        font-size: 24px;
        font-weight: 700;
        margin: 16px 0;
        color: var(--color-white);
    }

}

.card__body{
    width: 100%;
    margin-bottom: 20px;
}

.card__cta{
    width: 100%;


    button{
        width: 100%;
        border-radius: 28px;
        border: none;
        background-color: var(--color-orange);
        padding: 16px 0;
        color: var(--color-white);
        text-transform: uppercase;
        letter-spacing: 2px;
        font-weight: 700;

        &:active{
            background-color: var(--color-white);
            color: var(--color-white);
        }
    }
}

.rating__options{
    display: flex;
    justify-content: space-between;
    width: 100%;
    list-style: none;
    margin-top: 20px;

    .item{
        width: 40px;
        height: 40px;
        border-radius: 50%;
        background-color: var(--color-dark-blue-2);
        display: grid;
        justify-items: center;
        align-content: center;

        &--selected{
            color: var(--color-white);
            background-color: var(--color-orange);
        }
    }
}
</style>