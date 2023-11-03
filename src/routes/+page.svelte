<script>
    import CompleteBeginner from "$lib/workspace/CompleteBeginner.svelte";
    import Beginner from "$lib/complete/Beginner.svelte";
    import CompleteIntermediate from "$lib/workspace/CompleteIntermediate.svelte";
    import Intermediate from "$lib/complete/Intermediate.svelte";
    import CompleteAdvanced from "$lib/workspace/CompleteAdvanced.svelte";
    import Advanced from "$lib/complete/Advanced.svelte";


</script>

<main>
    <h1>Webページに挑戦！</h1>
    <h2>初級: 飾り文字を作ろう</h2>
    <div class="container">
        <div class="component">
            <CompleteBeginner/>
        </div>
        <div class="guideline">目安: 3分〜</div>
        <div class="component">
            <Beginner/>
        </div>
    </div>
    <h2>中級: カーソルを上に載せると動くボタンを作ろう</h2>
    <div class="container">
        <div class="component">
            <CompleteIntermediate/>
        </div>
        <div class="guideline">目安: 8分〜</div>
        <div class="component">
            <Intermediate/>
        </div>
    </div>
    <h2>上級: ハンバーガーメニューを作ろう</h2>
    <div class="container">
        <div class="component">
            <CompleteAdvanced/>
        </div>
        <div class="guideline">目安: 10分〜</div>
        <div class="component">
            <Advanced/>
        </div>
    </div>
</main>

<style>
    main {
        font-family: 'Noto Sans JP', sans-serif;
        color: #525252;
    }
    h1 {
        text-align: center;
        font-weight: bold;
    }
    h2 {
        text-align: center;
    }
    .container {
        display: flex;
        width: 100%;
        position: relative;
    }
    .container > .component:first-of-type:before {
        content: '見本';
        position: absolute;
        left: 10px;
        top: 10px;
        font-weight: bold;
        border-right: none;
    }
    .container > .component:last-of-type:before {
        content: '挑戦';
        position: absolute;
        left: 10px;
        top: 10px;
        font-weight: bold;
    }
    .guideline {
        position: absolute;
        right: 10px;
        top: 10px;
    }
    .component {
        width: 50%;
        height: 20svh;
        display: flex;
        justify-content: center;
        align-items: center;
        border: 1px solid rgb(128, 128, 128);
        position: relative;
    }
</style>