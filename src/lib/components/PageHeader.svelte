<script lang="ts">
    export let title:string = '';
</script>

<div>
    <h1>{title}</h1>
</div>

<style lang="scss">
    div{
        font-family: Arial, Helvetica, sans-serif;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 25px;
        h1{
            position: relative;
            overflow: hidden;
            padding-bottom: 1rem;
            &::after{
            content: '';
            background: var(--primary);
            height: 0.1em;
            width: 100%;
            margin-left: -100%;
            position: absolute;
            bottom: 0;
        }
        }
    }
</style>