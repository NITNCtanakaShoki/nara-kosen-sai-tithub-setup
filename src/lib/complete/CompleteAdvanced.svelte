<script>
    let isOpen = false;
    function toggle() {
        isOpen = !isOpen;
    }
</script>

<button class:open={isOpen} on:click={toggle}>
    <span/>
    <span/>
    <span/>
</button>

<style>
    button {
        width: 100px;
        height: 55px;

        background: none;

        outline: none;
        border: none;

        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-direction: column;
    }
    span {
        display: block;
        width: 100%;
        height: 15px;
        background: #6672ff;

        border-radius: 8px;
        transition: all 0.5s ease-in-out;
    }
    .open > span:first-of-type {
        transform: translateY(20px) rotate(405deg);
    }
    .open > span:nth-of-type(2) {
        opacity: 0;
    }
    .open > span:last-of-type {
        transform: translateY(-20px) rotate(-405deg);
    }
</style>