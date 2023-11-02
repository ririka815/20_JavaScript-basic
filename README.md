# 20_JavaScript-basic
 2023後期「JavaScript基礎」授業課題

## 授業内コード
1. 10月５日（木）はじめの一歩
2. 10月5日（木）GitHub　リポジトリ作成


### 11 月 2　日

- クリックイベント基本的な流れ

### クリックイベント基本的な流れ

```js
 const dacingBtn = document.querySelector(".dancing");
    const stopBtn = document.querySelector(".stop");
    const changeBtn = document.querySelector(".change");

    const dancer = document.querySelector(".imgArea img");

    //dacingBtnをクリックすると
    dacingBtn.addEventListener("click", function () {
         //dancerにclass="dance"が設定される
      dancer.setAttribute("class", "dance");
    });

    stopBtn.addEventListener("click", function () {
      dancer.removeAttribute("class");
    });

    changeBtn.addEventListener("click", function () {
      dancer.setAttribute("src", "images/ballet_woman.png");
      dancer.setAttribute("alt", "バレリーナいらすと");
    });

    //elem.setAttribute(name, value); //値を設定します。
    //elem.removeAttribute(name); //属性を削除します。
```


### 10 月　２6　日

- querySelectorAll
- getElementById
- getElementsByTagName, getElementsByClassName



### 10 月 19　日

- テンプレートリテラル
- 配列
- for文


### テンプレートリテラル
```js
console.log(`7 ✕ ${i + 1} = ${7 * (i + 1)}`);
```

### 配列
```js
 //宣言・代入
 //["0", "1", "2"]
        const animals = ["dog", "cat", "bird"];

        //確認
        console.log(animals);
        //長さ
        console.log(animals.lenght);
        //cat
        console.log(animals[1]);
```

### for文
```js
//i < fruits.length;はリスト全部を指定することができる
for (let i = 0; i < fruits.length; i++) {
            //liに創出する
            //createElementはもともとただの文字だったものをliに変換してHTMにliとして読み込むために使う
            const lilast = document.createElement("li");

            //liに値（果物・配列fruitsの中にある）を代入
            console.log(fruits[i]);//りんご・もも・バナナが取れる

            //算出したliの内容に果物を代入
            lilast.textContent = fruits[i];

            //ul内の最後に追加
//elementの中にlilastを追加する
            element.appendChild(lilast);
        }
```


## 10 月　12 日　

- リテラルと演算子
- 文字列の計算
- 変数の宣言
- 定数の宣言
- 複合代入演算子
- インクリメント
- 文字列の扱い

- リストを操作するDOM操作のスクリプト

### 文字列の計算

```js
//文字列の連結
console.log("ABC" + "DEF"); //文字列　＋　文字列
        console.log("円周率は" + 3.14 + "です"); //文字列　＋　数値
        console.log("計算結果：" + 123 + 456); //文字列　＋　数値の計算
        console.log(123 + 456 + "となりました"); //数次の計算　＋　文字列
        console.log("計算結果：" + (123 + 456)); //文字列　＋　（数値の計算）
        console.log("2" - 1); //文字列　ー　数値
        console.log("2" * 3); //文字列　ー　数値
        console.log("2" / 4); //文字列　ー　数値
```

### 変数の宣言
```js
//文字列の連結
//let a; //変数の宣言
  a = 10; //値の代入(数値型)
     console.log(a);

       a = "Hello"; //値の再代入（文字列型）
      console.log(a);

      let a = "World"; //変数の宣言と代入を同時に行っています。更に再宣言なのでエラーとなります。
```

### 定数の宣言
```js
const PI = 3.14;
        console.log(PI);

      再代入
         PI = 3.1415926535;
         const PI;
```

### 複合代入演算子
```js
let n = 5;
        n = n + 2;
        console.log(n);

        let n2 = 5;
        n2 += 2; //複合代入演算子　n2 = n2 +2 と同じ
        console.log(n2);
```

### インクリメント　
```js
let n3 = 5;
        n3++; //インクリメント　１足す
        console.log(n3); //6
```

### 文字列の扱い
```js
let s = "Hello";
console.log(s.toUpperCase());//文字を表示
console.log(s.length);//文字数
```




### リストを操作するDOM操作のスクリプト
```js
//メロンを加えたい
        //ul要素を取り入れる

        const element = document.querySelector("ul");
        console.log(element);

        //selectorってCSSのセレクターなので
        const element2 = document.querySelector("#fruitslist");
        console.log(element2);

        //classも行ける
        const element3 = document.querySelector(".listbox__list");
        console.log(element3);

        const lilast = document.createElement("li");
        console.dir(lilast);//dirに変更。オブジェクトの中身が見える。
        lilast.textContent = "メロン";
        console.log(lilast);
```


## 10 月 5 日

- インターネットの基本について理解する。
- Web の基本的な仕組みを理解する。
- Web サーバーの役割について理解する。
- 開発環境の構築
- JavaScript を書く場所

### JavaScript を書く場所

1. HTML ファイルの中
1. 外部 JS ファイルの中
1. ブラウザのコンソール

基本は、外部 JS ファイルを読み込むが、HTML 内に各場合は、`</body>`の上に書く。

```html
<!doctype html>
<html lang=ja>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>演習</title>
</head>
<body>
</script>
</body>
</html>
```

### フロントエンドロードマップ

フロントエンドエンジニアに必要なスキルの[ロードマップ](https://roadmap.sh/frontend)がある。