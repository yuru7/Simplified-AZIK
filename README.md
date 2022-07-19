# Simplified-AZIK

Simplified-AZIKは、ローマ字入力拡張のAZIKから使いやすい要素を限定的に抽出し、さらに従来のローマ字入力に完全な互換性を持つことを目指した、シンプルな使い勝手のAZIKインスパイアな入力方式です。

本リポジトリでは、Google日本語入力のローマ字テーブル設定ファイルを提供します。

## AZIKとは

AZIKは、「ローマ字入力の経験を活かしつつ、入力効率を上げる」ことに着目した、ローマ字入力の拡張定義です。そういったコンセプトから、ローマ字入力に慣れた方が少ない習熟コストで習得できるのが特徴です。

AZIKでは基本のローマ字入力方式は出来るだけそのままに、日本語での頻出パターンの入力を短縮化するように独自のアルファベットの組み合わせが拡充されています。

※AZIKの基本的な入力方法については、AZIK開発者による [AZIK総合解説書](http://hp.vector.co.jp/authors/VA002116/azik/azikinfo.htm) を参照してください。

## Simplified-AZIKが目指すもの

AZIKはローマ字入力の拡張系ではあるものの、その互換性は完全なものではありません。入力効率を高めるために元のローマ字入力方式から一部の互換性が失われています。

Simplified-AZIKでは、 **従来のローマ字入力との互換性を完全に保つ** ことを最優先にしています。その上でAZIK独自の撥音（ん）の入力方法など、AZIKの特徴的な機能を取り入れています。

そのため、既にローマ字入力が出来る人がSimplified-AZIKを使い始めるにあたり必要となる知識はありません。まずは通常通りに使い、撥音（ん）や二重母音を入力するタイミングで少しずつ拡張された入力方法を取り入れていきましょう。

## インストール

[Simplified-AZIK.txt](./Simplified-AZIK.txt) をダウンロードして、 `Google日本語入力 プロパティ > ローマ字テーブル [編集]ボタン > 編集 > インポート` を実行し、当該ファイルを読み込んでください。

## Simplified-AZIKで拡張されるローマ字テーブル

- `*z = ann` `*k = inn` `*j = unn` `*d = enn` `*l = onn` で撥音（ん）の入力
  - 例: `skkzsd = しんかんせん`
- `*q = ai` `*c = ei` `*r = uu` `*t = ui` `*, = ie` `*p = ou` で二重母音を入力
  - 例: `kqtcnoryrgrjp = かいていのりゅうぐうじょう`
- 上記にて子音が二重になる場合は、2文字目は `;` で代用する
  - 例: 「ざん」と入力しようとする場合、 `zz` ではなく `z;` と入力する
- `xa = しゃ` `xu = しゅ` `xo = しょ` `ca = ちゃ` `cu = ちゅ` `co = ちょ` の追加
- 省略入力の追加
  - `ds = です` `ms = ます`
