# 環境構築ガイド

Vue.js と Vuetify の開発を始めるための環境構築手順を説明します。

## 前提条件

- Visual Studio Code (VSCode) がインストールされていること
- インターネット接続があること

## 必要な拡張機能

### 1. Volar (Vue Language Features)

Vuter は廃止され、現在は **Volar** が Vue.js の公式推奨拡張機能です。

**機能:**
- Vue ファイルのシンタックスハイライト
- インテリセンス（コード補完）
- 型チェック
- Vue 3 の Composition API のサポート

**インストール方法:**

1. VSCode を開く
2. 左サイドバーの拡張機能アイコンをクリック（またはCtrl+Shift+X）
3. 検索ボックスに「Vue Language Features (Volar)」と入力
4. 「Vue Language Features (Volar)」を見つけてインストールをクリック
5. 必要に応じて VSCode を再起動

**拡張機能ID:** `Vue.volar`

**注意:** もし以前に Vuter をインストールしている場合は、競合を避けるためにアンインストールしてください。

---

### 2. HTMLHint

HTML ファイルの文法エラーや問題を検出してくれる Linter です。

**機能:**
- HTML の文法チェック
- アクセシビリティの問題を検出
- ベストプラクティスの提案

**インストール方法:**

1. VSCode の拡張機能パネルを開く
2. 「HTMLHint」と検索
3. インストールをクリック

**拡張機能ID:** `HTMLHint.vscode-htmlhint`

**設定（オプション）:**

プロジェクトルートに `.htmlhintrc` ファイルを作成することでルールをカスタマイズできます。

```json
{
  "tagname-lowercase": true,
  "attr-lowercase": true,
  "attr-value-double-quotes": true,
  "doctype-first": true,
  "tag-pair": true,
  "spec-char-escape": true,
  "id-unique": true,
  "src-not-empty": true,
  "attr-no-duplication": true,
  "title-require": true
}
```

---

### 3. Prettier - Code formatter

コードの自動フォーマッターです。一貫したコードスタイルを保つことができます。

**機能:**
- HTML, CSS, JavaScript, Vue ファイルの自動フォーマット
- 保存時に自動フォーマット（設定で有効化可能）
- チーム全体で統一されたコードスタイル

**インストール方法:**

1. VSCode の拡張機能パネルを開く
2. 「Prettier - Code formatter」と検索
3. インストールをクリック

**拡張機能ID:** `esbenp.prettier-vscode`

**設定方法:**

VSCode の設定で Prettier をデフォルトのフォーマッターに設定します。

1. VSCode で `Ctrl+,` を押して設定を開く
2. 検索ボックスに「default formatter」と入力
3. 「Editor: Default Formatter」を「Prettier - Code formatter」に設定
4. 検索ボックスに「format on save」と入力
5. 「Editor: Format On Save」にチェックを入れる

**または、settings.json に直接追加:**

`Ctrl+Shift+P` → 「Preferences: Open Settings (JSON)」を選択

```json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "[html]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[vue]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  }
}
```

**Prettier 設定ファイル（オプション）:**

プロジェクトルートに `.prettierrc` ファイルを作成することでフォーマットルールをカスタマイズできます。

```json
{
  "semi": true,
  "singleQuote": true,
  "tabWidth": 2,
  "useTabs": false,
  "printWidth": 100,
  "trailingComma": "es5"
}
```

---

### 4. Emmet（エメット）

Emmet は HTML と CSS を高速で記述するためのツールです。**VSCode にはデフォルトで組み込まれている**ため、追加のインストールは不要です！

**機能:**
- 省略記法で HTML を素早く生成
- CSS セレクタのような記法で HTML を書ける
- Tab キーで展開
- 入れ子構造も簡単に作成

**基本的な使い方:**

Emmet の省略記法を入力して、`Tab` キーを押すと HTML に展開されます。

**例1: 基本的なタグ**
```
div [Tab]
→ <div></div>

p [Tab]
→ <p></p>
```

**例2: クラス名付き**
```
div.container [Tab]
→ <div class="container"></div>

p.text-center [Tab]
→ <p class="text-center"></p>
```

**例3: ID 付き**
```
div#app [Tab]
→ <div id="app"></div>
```

**例4: 複数のクラス**
```
div.card.shadow [Tab]
→ <div class="card shadow"></div>
```

**例5: 入れ子構造（子要素）**
```
div>p [Tab]
→ <div>
    <p></p>
  </div>

ul>li [Tab]
→ <ul>
    <li></li>
  </ul>
```

**例6: 兄弟要素**
```
div+p [Tab]
→ <div></div>
  <p></p>
```

**例7: 繰り返し**
```
ul>li*5 [Tab]
→ <ul>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
  </ul>
```

**例8: テキスト挿入**
```
p{Hello World} [Tab]
→ <p>Hello World</p>

a{リンク} [Tab]
→ <a href="">リンク</a>
```

**例9: 属性の追加**
```
a[href="https://vuejs.org" target="_blank"] [Tab]
→ <a href="https://vuejs.org" target="_blank"></a>

img[src="image.jpg" alt="説明"] [Tab]
→ <img src="image.jpg" alt="説明">
```

**例10: 複雑な構造**
```
div.container>header>h1{タイトル}+nav>ul>li*3>a{メニュー$} [Tab]
→ <div class="container">
    <header>
      <h1>タイトル</h1>
      <nav>
        <ul>
          <li><a href="">メニュー1</a></li>
          <li><a href="">メニュー2</a></li>
          <li><a href="">メニュー3</a></li>
        </ul>
      </nav>
    </header>
  </div>
```

**よく使う Emmet 記法まとめ:**

| 記法 | 説明 | 例 |
|------|------|------|
| `>` | 子要素 | `div>p` |
| `+` | 兄弟要素 | `div+p` |
| `*` | 繰り返し | `li*5` |
| `.` | クラス | `div.container` |
| `#` | ID | `div#app` |
| `[]` | 属性 | `a[href="#"]` |
| `{}` | テキスト | `p{Hello}` |
| `$` | 番号（連番） | `li{Item $}*3` |
| `^` | 親要素に戻る | `div>p>span^div` |

**HTML5 のテンプレート:**

VSCode で `!` と入力して `Tab` を押すと、HTML5 の基本テンプレートが生成されます：

```
! [Tab]
→ <!DOCTYPE html>
  <html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
  </head>
  <body>
    
  </body>
  </html>
```

**練習問題:**

以下の Emmet 記法を試してみましょう：

1. `table>tr*3>td*4` - 3行4列のテーブル
2. `form>input[type="text"]+button{送信}` - フォーム
3. `ul.menu>li.menu-item*4>a[href="#"]{リンク$}` - メニューリスト

**Emmet のメリット:**
- ⚡ HTML を**10倍速く**書ける
- 🎯 タイプミスが減る
- 📝 複雑な構造も簡単に作成
- 🚀 生産性が大幅に向上

Emmet を使いこなすと、HTML のコーディングが劇的に速くなります！

---

## 動作確認

すべての拡張機能がインストールされたら、以下の方法で動作を確認してください。

### Volar の確認
- `.vue` ファイルを開いて、シンタックスハイライトが正しく動作するか確認
- `<script>` タグ内でコード補完が動作するか確認

### HTMLHint の確認
- HTML ファイルで意図的に間違った HTML を書いてみる（例: 閉じタグを書かない）
- 波線でエラーが表示されるか確認

### Prettier の確認
- HTML や JavaScript ファイルでインデントを不揃いにする
- ファイルを保存（Ctrl+S）して自動的にフォーマットされるか確認

---

## トラブルシューティング

### Volar が動作しない
- VSCode を再起動してください
- Vuter がインストールされている場合は無効化またはアンインストールしてください

### Prettier が動作しない
- デフォルトフォーマッターが正しく設定されているか確認
- 「Format On Save」が有効になっているか確認
- 右クリック → 「フォーマット」を手動で実行してみる

### HTMLHint が動作しない
- `.htmlhintrc` ファイルの構文が正しいか確認
- VSCode を再起動してみる

---

## 次のステップ

環境構築が完了したら、次のハンズオンに進みましょう！

1. **01-html-basic.html** - 基本的な HTML 要素の書き方
2. **02-javascript-events.html** - JavaScript と input 要素のイベント処理
3. **03-vue-basic.html** - Vue.js の基本的な書き方
4. **04-vue-advanced.html** - Vue.js の応用（v-if, v-for など）
5. **05-vuetify-basic.html** - Vuetify の基本的な使い方

それでは、楽しく学習していきましょう！ 🚀

