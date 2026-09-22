# recipe-cards

レシピカード HTML の GitHub Pages ホスト。

- サイト: https://1000says.github.io/recipe-cards/
- リポ: https://github.com/1000says/recipe-cards
- カード規約: `https://1000says.github.io/recipe-cards/cards/<slug>.html`

現状の1枚:

- [牡丹鰺と翡翠茄子のお碗](https://1000says.github.io/recipe-cards/cards/botan-hamo-hisui-nasu.html)

## 公開 / 非公開の切替

切替の本体は **リポジトリの Visibility**。`visibility.json` の `mode` は意図の記録。

### UI

1. https://github.com/1000says/recipe-cards/settings
2. 一番下 Danger zone → **Change visibility**
3. Public または Private を選ぶ

### CLI

```bash
# 公開（Pages が誰でも開く）
gh repo edit 1000says/recipe-cards --visibility public --accept-visibility-change-consequences

# 非公開（ソースは見えない）
gh repo edit 1000says/recipe-cards --visibility private --accept-visibility-change-consequences
```

| 状態 | ソース | Pages |
|---|---|---|
| public | 誰でも読める | `*.github.io/recipe-cards/` が公開 |
| private（無料） | 自分だけ | Pages は止まる |
| private（GitHub Pro） | 自分だけ | 私設 Pages が使える |

無料プランで非公開にすると URL は死ぬ。再び公開すれば戻る。

## 初回だけ必要な Pages 設定

Actions の初回デプロイが落ちたときは:

1. Settings → Pages
2. Source を **GitHub Actions** にする
3. 失敗した workflow を Re-run

ワークフロー: `.github/workflows/pages.yml`（main への push と手動実行）。

## Todoist への載せ方

description 先頭:

```
[カード HTML] https://1000says.github.io/recipe-cards/cards/<slug>.html
ショートカット: 上のURLを開く
```
