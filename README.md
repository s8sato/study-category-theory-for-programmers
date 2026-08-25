# 圏論入門（Category Theory for Programmers・抜粋）

Bartosz Milewski 著 *Category Theory for Programmers* の Part One（基礎編）から、Web系ソフトウェア開発者が学ぶ価値の高いトピックだけを厳選し、日本語でまとめた学習ノート集です。数式は最小限にとどめ、身近なプログラミングの例（Haskell の型と関数）との対応を重視しています。

## 公開サイト

このリポジトリの `vault/` は [Obsidian](https://obsidian.md/) vault で、[enastro](https://github.com/s8sato/enastro) によって静的サイトへビルドされ、GitHub Pages で自動公開されています（`main` ブランチへの push で [.github/workflows/deploy.yml](.github/workflows/deploy.yml) が実行されます）。

- 公開サイト: https://s8sato.github.io/study-category-theory-for-programmers/

## 対象読者

- Webアプリケーション開発の実務経験があるが、圏論・抽象代数は初めて、という人
- Haskell などの関数型言語の Functor / Applicative といった用語の「裏付け」を知りたい人

## 読む順番の目安

1. [圏](vault/圏.md) — 圏論全体の出発点。対象・射・合成・恒等射という4つの部品から成り立つこと。
2. [積](vault/積.md) — 2つの対象を「組み合わせる」普遍的な方法。余積とはペアの概念。
3. [関手](vault/関手.md) — 圏と圏の間の構造を保つ写像。プログラミングでは `Functor` 型クラスに対応。

詳しい全体構成は [圏論入門-hub](vault/圏論入門-hub.md) を参照してください。

## 範囲外にしたもの

モナド・随伴・米田の補題など Part Two 以降の話題は、本ノート群では扱いません（将来の拡張候補）。

## 出典・ライセンスについて

本ノート群は、Bartosz Milewski 著 *Category Theory for Programmers*（[原著サイト](https://bartoszmilewski.com/2014/10/28/category-theory-for-programmers-the-preface/)、CC BY-NC-ND ライセンス）を出典とし、その内容を要約・翻訳・再構成した非公式な個人の学習ノートです。原著の公式な翻訳・派生物ではありません。
