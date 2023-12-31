<template>
<svg fill="var(--bs-light)" viewBox="0 0 100 60" width="48">
    <rect width="80" height="10" x="10" y="0" rx="4"></rect>
    <rect width="80" height="10" x="10" y="25" rx="4"></rect>
    <rect width="80" height="10" x="10" y="50" rx="4"></rect>
</svg>
</template>

<style lang="scss">
svg{
    --duration: 220ms;
    rect{
        transition: y var(--duration) ease-in var(--duration),
                    rotate var(--duration) ease-in,
                    opacity 0ms var(--duration);
        transform-origin: center;
    }
    &:hover{
        rect{
            transition: y var(--duration) ease-in,
                    rotate var(--duration) ease-in var(--duration),
                    opacity 0ms var(--duration);
            &:is(:first-child, :last-child){
                y: 25;
            }
            &:first-child{
                rotate: 45deg;
            }
            &:nth-child(2){
                opacity: 0;
            }
            &:last-child{
                rotate: -45deg;
            }
        }
    }
}
</style>
