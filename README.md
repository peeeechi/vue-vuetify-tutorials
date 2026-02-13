# Vue.js & Vuetify ハンズオン教材

Web 開発初心者向けの Vue.js と Vuetify のハンズオン教材です。

## 🌐 GitHub Pages で見る

このハンズオン教材は GitHub Pages で公開されています：

👉 **[ハンズオン教材サイトを開く](https://peeeechi.github.io/vue-vuetify-tutorials/)**

## 📚 学習コンテンツ

### 0. 環境構築

**ファイル**: [`hands-on/00-setup.md`](./hands-on/00-setup.md)

VSCode の拡張機能のインストールと設定方法を学びます。

- **Volar (Vue Language Features)** - Vue.js の公式拡張機能
- **HTMLHint** - HTML の Linter
- **Prettier** - コードフォーマッター
- **Emmet** - HTML を高速に書くための省略記法（VSCode に標準搭載）

**追加**: [`hands-on/00-emmet-practice.html`](./hands-on/00-emmet-practice.html) - Emmet の練習ページ

Emmet の省略記法を実際に試せる練習用ページです。レベル別の課題とチートシート付き！

### 1. 基本的な HTML 要素

**ファイル**: [`hands-on/01-html-basic.html`](./hands-on/01-html-basic.html) | [📖 ブラウザで開く](https://peeeechi.github.io/vue-vuetify-tutorials/hands-on/01-html-basic.html)

Web ページを作成する上で基本となる HTML 要素を学習します。

- **見出し** (h1〜h6)
- **リスト** (ul, ol)
- **テーブル** (table)
- **水平線** (hr)
- **コンテナ** (div)
- **リンク** (a)
- **Emmet** - HTML を10倍速く書く方法
  - 省略記法の基本
  - よく使う記号（`>`, `+`, `*`, `.`, `#`, `[]`, `{}`）
  - 実践的な使い方
  - 複雑な構造を一行で生成

### 2. JavaScript とイベント処理

**ファイル**: [`hands-on/02-javascript-events.html`](./hands-on/02-javascript-events.html) | [📖 ブラウザで開く](https://peeeechi.github.io/vue-vuetify-tutorials/hands-on/02-javascript-events.html)

JavaScript を使って HTML 要素にインタラクティブな機能を追加する方法を学びます。

- **DOM の操作**
  - `getElementById()`, `querySelector()`
- **イベント処理**
  - `addEventListener()`
  - click, input, change イベント
- **フォーム要素**
  - テキストボックス
  - チェックボックス
  - ラジオボタン
  - セレクトボックス
- **実践例**
  - 文字数カウンター
  - 簡単な計算機
  - フォームバリデーション

### 3. Vue.js の基本

**ファイル**: [`hands-on/03-vue-basic.html`](./hands-on/03-vue-basic.html) | [📖 ブラウザで開く](https://peeeechi.github.io/vue-vuetify-tutorials/hands-on/03-vue-basic.html)

Vue.js を使って、簡単にインタラクティブな Web アプリケーションを作成する方法を学習します。

- **Vue.js とは？**
  - リアクティブなフレームワーク
  - Vanilla JS との比較
- **CDN 方式でのセットアップ**
- **v-model** - 双方向データバインディング
- **v-bind / :** - 属性のバインディング
- **イベントハンドリング**
  - `@click`, `@input`, `@change`
- **マスタッシュ構文** - `{{ 変数名 }}`
- **methods** - メソッドの定義
- **チェックボックスとの連携**

### 4. Vue.js の応用

**ファイル**: [`hands-on/04-vue-advanced.html`](./hands-on/04-vue-advanced.html) | [📖 ブラウザで開く](https://peeeechi.github.io/vue-vuetify-tutorials/hands-on/04-vue-advanced.html)

Vue.js の条件分岐、ループ、その他の便利な機能を学習します。

- **v-if / v-else-if / v-else** - 条件分岐
- **v-show** - 表示/非表示の切り替え
- **v-if と v-show の違い**
- **v-for** - ループ処理
  - 配列のループ
  - オブジェクト配列のループ
  - `:key` 属性の重要性
- **computed** - 算出プロパティ
- **フィルタリング機能**
- **実践: To-Do リストアプリ**
  - タスクの追加・削除
  - 完了/未完了の管理
  - 統計情報の表示

### 5. Vuetify の基本

**ファイル**: [`hands-on/05-vuetify-basic.html`](./hands-on/05-vuetify-basic.html) | [📖 ブラウザで開く](https://peeeechi.github.io/vue-vuetify-tutorials/hands-on/05-vuetify-basic.html)

Vuetify を使って、美しい Material Design の UI を簡単に構築する方法を学びます。

- **Vuetify とは？**
  - Material Design コンポーネントフレームワーク
- **CDN 方式でのセットアップ**
- **主要コンポーネント**
  - **v-btn** - ボタン
  - **v-text-field** - テキスト入力
  - **v-card** - カードレイアウト
  - **v-list** - リスト
  - **v-chip** - チップ（タグ）
  - **v-alert** - アラートメッセージ
  - **v-form** - フォーム
  - **v-data-table** - データテーブル
- **実践例**
  - ユーザー登録フォーム
  - データテーブルでのユーザー管理

## 🚀 学習の進め方

### ステップ 1: 環境構築

1. `hands-on/00-setup.md` を読んで、VSCode の拡張機能をインストールします
2. 各拡張機能が正しく動作することを確認します

### ステップ 2: 順番に学習

各 HTML ファイルを順番に開いて学習してください。

```
hands-on/01-html-basic.html
  ↓
hands-on/02-javascript-events.html
  ↓
hands-on/03-vue-basic.html
  ↓
hands-on/04-vue-advanced.html
  ↓
hands-on/05-vuetify-basic.html
```

### ステップ 3: ブラウザで確認

各 HTML ファイルをブラウザで開いて、実際に動作を確認しながら学習します。

**開き方（VSCode を使用している場合）:**

1. HTML ファイルを右クリック
2. "Open with Live Server" を選択（Live Server 拡張機能が必要）

または

1. HTML ファイルをダブルクリック
2. デフォルトのブラウザで開く

### ステップ 4: 演習問題に挑戦

各ファイルの最後にある演習問題に挑戦して、理解を深めます。

## 📖 参考リソース

### 公式ドキュメント

- **Vue.js**: https://ja.vuejs.org/
- **Vuetify**: https://vuetifyjs.com/
- **MDN Web Docs**: https://developer.mozilla.org/ja/

### 学習リソース

- **Vue.js 入門**: https://ja.vuejs.org/guide/introduction.html
- **Vuetify コンポーネント**: https://vuetifyjs.com/en/components/all/

## 💡 ヒント

### デバッグ方法

1. **ブラウザの開発者ツール**
   - Chrome: F12 キー
   - Firefox: F12 キー
   - Safari: Command + Option + I (Mac)

2. **console.log() を使う**
   ```javascript
   console.log('変数の値:', this.myVariable);
   ```

3. **Vue Devtools を使う**
   - Chrome/Firefox の拡張機能
   - Vue アプリのデータ構造を可視化

### よくあるエラー

1. **CDN が読み込まれていない**
   - インターネット接続を確認
   - ブラウザのキャッシュをクリア

2. **Vue が動作しない**
   - `<v-app>` で囲んでいるか確認（Vuetify の場合）
   - `.mount('#app')` の ID が正しいか確認

3. **イベントが動作しない**
   - `@click` のスペルミスがないか確認
   - メソッド名が正しいか確認

## 🎯 学習目標

このハンズオンを完了すると、以下のことができるようになります：

✅ 基本的な HTML 要素を使ってページを作成できる  
✅ JavaScript でイベント処理ができる  
✅ Vue.js でリアクティブなアプリケーションを作成できる  
✅ v-if, v-for などの Vue ディレクティブを使いこなせる  
✅ Vuetify で美しい UI を簡単に構築できる  
✅ フォームバリデーションができる  
✅ データテーブルでデータを管理できる

## 📝 演習課題のアイデア

ハンズオンを終えた後、以下のようなアプリケーションを作成してみましょう：

1. **タスク管理アプリ**
   - タスクの追加・削除・編集
   - 優先度の設定
   - フィルタリング機能

2. **買い物リストアプリ**
   - 商品の追加・削除
   - 価格の計算
   - カテゴリー分類

3. **簡単な日記アプリ**
   - 日付付きエントリーの追加
   - 検索機能
   - タグ付け

4. **問い合わせフォーム**
   - バリデーション付きフォーム
   - 入力内容の確認画面
   - 送信完了メッセージ

## 🤝 サポート

質問や不明点があれば、遠慮なく質問してください！

Happy Learning! 🎉
