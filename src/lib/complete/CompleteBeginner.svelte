<h1>Colorful Letter</h1>

<style>
    h1 {
        /* 文字の大きさを指定する */
        font-size: 24px;

        /* 背景を七色のグラデーションに設定する */
        background: linear-gradient(45deg, red, orange, yellow, green, blue, midnightblue, purple);

        /** 文字色を透明にする */
        color: transparent;

        /** 背景を文字の形に切り抜く */
        background-clip: text;
        -webkit-background-clip: text;

        /** 下に反射をつける */
        -webkit-box-reflect: below -10px -webkit-gradient(linear, left bottom, left top, from(transparent), to(white));

        /** 文字に影をつける */
        text-shadow: 2px 2px 3px rgba(0, 0, 0, 0.2);
    }
</style>
