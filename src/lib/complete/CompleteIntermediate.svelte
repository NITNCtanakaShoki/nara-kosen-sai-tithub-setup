<button>Button</button>

<style>
    button {
        width: 200px;
        height: 70px;

        background-color: white;

        font-size: 24px;

        border: 1px solid black;

        position: relative;

        color: black;
        z-index: 1;

        overflow: hidden;
        transition: color 0.2s ease;
    }
    button:before {
        content: '';

        display: block;
        width: 100%;
        height: 100%;
        background-color: black;

        position: absolute;
        left: 0;
        top: 0;

        z-index: -1;

        transform: translateX(-100%);

        transition: transform 0.2s ease-in-out;
    }
    button:hover {
        color: white;
    }
    button:hover:before {
        transform: translateX(0);
    }
</style>