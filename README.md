# 生成AIパスポート試験問題アプリ

生成AIパスポート試験の学習を支援するWebアプリケーションです。  
模擬試験・問題一覧・教科書機能を提供し、効率的な試験対策をサポートします。

---

# Live Demo

ブラウザからすぐ利用できます（インストール不要）

https://yusuke-narusaka.github.io/ai-app/

---

# 概要

このアプリは、生成AIパスポート試験の学習補助を目的として開発された  
**ブラウザベースの学習アプリ**です。

以下の機能により、試験対策を効率化します。

- 模擬試験機能
- 分野別問題一覧
- 教科書型学習コンテンツ
- 過去結果の保存

---

# 主な機能

## 模擬試験

- 問題数を指定して模擬試験を実施（1〜60問）
- 制限時間付き試験
- 解答後すぐに正誤判定
- 詳細な解説表示
- 結果の自動保存
- 進捗バー表示

---

## 問題一覧

試験範囲の問題を **階層構造で閲覧可能**

構造


章
└ セクション
└ サブセクション
└ 学習項目


機能

- 問題数表示
- 問題文閲覧
- 選択肢表示
- 正解確認
- 詳細解説

パンくずリストにより階層移動が可能です。

---

## 教科書機能

試験範囲の学習コンテンツを閲覧できます。

構造


章
└ セクション
└ 学習項目


機能

- 学習目標表示
- 詳細な解説
- 階層ナビゲーション

---

## 過去結果

模擬試験の履歴を確認できます。

表示内容

- 実施日
- 正解数
- 正答率

さらに

- 試験内容の詳細確認
- 回答履歴
- 解説確認
- 結果の削除

が可能です。

---

# 動作環境

以下のブラウザで動作します。

- Google Chrome
- Firefox
- Microsoft Edge
- Safari

---

# ファイル構成


ai-app
│
├ index.html
├ styles.css
│
├ main.js
├ quiz.js
├ questions.js
├ pastResults.js
├ questionList.js
├ textbook.js
├ textbookContent.js
├ utils.js
│
└ README.md


---

# 問題の追加方法

問題データは


questions.js


に定義されています。

新しい問題を追加する場合は  
`allQuestions` 配列にオブジェクトを追加します。

例

```javascript
{
  id: "XXX",
  chapter: "章タイトル",
  section: "セクション",
  subsection: "サブセクション",
  learningItem: "学習項目",
  Quiz: "問題文",
  Answer: "1",
  Choice: [
    "1 選択肢A",
    "2 選択肢B",
    "3 選択肢C",
    "4 選択肢D"
  ],
  Description: "解説"
}
教科書コンテンツ追加

教科書データは


textbookContent.js


に定義されています。

構造


章
 └ sections
    └ learningItems


例

{
  title: "学習項目タイトル",
  paragraphs: [
    "段落1",
    "段落2"
  ]
}
技術スタック

HTML

CSS

JavaScript

GitHub Pages

免責事項

このアプリは生成AIパスポート試験の学習補助を目的としています。
試験内容の正確性や合格を保証するものではありません。

開発者

鳴坂祐佑

GitHub
https://github.com/yusuke-narusaka
