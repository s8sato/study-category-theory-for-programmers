---
publish: true
tags: [programming]
---

# HaskellのFunctor型クラス

Haskellの `Functor` 型クラスは、[[関手]] の概念をそのままプログラミング言語の機能として実装したものです。

```haskell
class Functor f where
  fmap :: (a -> b) -> f a -> f b
```

ここで `f` は型コンストラクタ（`Maybe`、`[]`、`Either e` など）であり、[[圏]] における関手の「対象を対象に写す」部分は `f` 自身が、「射を射に写す」部分は `fmap` が担っています。この `f` は必ず [[Hask圏]] から自分自身への自己関手になります。

たとえば `Maybe` の場合、`fmap` は「値があれば関数を適用し、`Nothing` ならそのまま何もしない」という振る舞いになります。

```haskell
fmap (+1) (Just 3)  -- Just 4
fmap (+1) Nothing   -- Nothing
```

この型クラスが妥当な `Functor` として認められるためには、[[関手則]] を満たす必要があります。GHCコンパイラはこの法則を強制しませんが、`DeriveFunctor` 拡張を使えば、法則を自動的に満たすインスタンスを導出できます。
