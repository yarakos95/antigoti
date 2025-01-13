# antigoti パッケージ

ひらがな・カタカナに明朝体、漢字にゴシック体を当てることでアンチゴチを作成する LaTeX パッケージです。

![test image](./test/image-png/test-image-1.png)

## 要件

- LuaLaTeX＋luatexja
- expl3

## パッケージ読み込み

```latex
\usepackage{antigoti}
```

### パッケージオプション

| オプション | 値           | 説明                        |
| :--------: | ------------ | --------------------------- |
|    `bf`    | boolean      | 全体に `\bfseries` を課すか |
|   `font`   | フォント命令 | 各文字のフォント命令の指定  |
|  `color`   | 色           | 色を指定                    |

`bf` を使用する場合は、luatexja-preset パッケージの `deluxe` オプションを有効にして多書体化してください。

`font`・`color` オプションは次のように `kana`、`kanji`、`latin`、`other` の 4 つの値それぞれにフォント命令や色を指定します。

```latex
\usepackage[
  font =
  {
    other = \sffamily,
  },
  color =
  {
    kana = red,
    kanji = blue,
  }
]{antigoti}
```

ただし、`color` で指定できる色は `black`、`white`、`red`、`green`、`blue`、`cyan`、`magenta`、`yellow` の 8 つです。もしも自由に色を指定したい場合は `\color_set:nn` を構成してください。

## 使い方

antigoti パッケージが提供するコマンドは 1 つです。

```latex
\antigoti{〈文章〉}
```

パッケージオプションと同様のオプションを利用できます。

## LICENSE

MIT License
