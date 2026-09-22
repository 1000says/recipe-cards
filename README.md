# recipe-cards

レシピカード HTML の GitHub Pages ホスト。

- サイト: https://1000says.github.io/recipe-cards/
- リポ: https://github.com/1000says/recipe-cards

## 公開 / 非公開

切替はリポの Visibility。

```bash
# 公開（Pages が誰でも開く）
gh repo edit 1000says/recipe-cards --visibility public --accept-visibility-change-consequences

# 非公開（ソースは見えない。Pages は GitHub Pro の私設 Pages が要る）
gh repo edit 1000says/recipe-cards --visibility private --accept-visibility-change-consequences
```

現状は public。`visibility.json` の `mode` を実態に合わせる。

## URL規約

`https://1000says.github.io/recipe-cards/cards/<slug>.html`
