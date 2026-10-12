# hagikrua.com

「萩倉」を題字として表示するシンプルな Web ページです。

PC では横書き、スマートフォンでは縦書きで表示します。

## Font

このサイトでは、青柳衡山氏による **衡山毛筆フォント行書** を使用しています。

- Font: 衡山毛筆フォント行書
- Author: 青柳衡山
- Distribution: 武蔵システム
- Official page: https://opentype.jp/kouzangyousho.htm

公式配布ページでは、以下の条件で利用可能とされています。

- 無料で利用可能
- 商用利用可能
- ロゴ等への利用可能
- 雑誌・書籍への掲載、CD 等への収録可能
- 無保証

本リポジトリでは、元の OpenType フォント `KouzanGyoushoOTF.otf` から、Web ページで使用する「萩倉」の文字のみを抽出し、WOFF2 形式へサブセット化したフォントを使用しています。

```text
fonts/KouzanGyousho-Hagikura.woff2
```

サブセット化には [fontTools](https://github.com/fonttools/fonttools) の `pyftsubset` を使用しています。

```sh
pyftsubset KouzanGyoushoOTF.otf \
  --text="萩倉" \
  --flavor=woff2 \
  --output-file=KouzanGyousho-Hagikura.woff2
```

フォントの利用条件については、配布元の最新情報を確認してください。

## Structure

```text
.
├── index.html
├── README.md
└── fonts/
    └── KouzanGyousho-Hagikura.woff2
```
