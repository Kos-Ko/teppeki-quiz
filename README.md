# 鉄壁 Section 1〜50 文脈穴埋め確認テスト

大学受験英語の語彙を、文脈の中で確認するための4択テスト（全10問）です。
選択肢を押すと、その場で正誤と解説が表示されます。

## 🔗 テストを開く（GitHub Pages）

**https://YOUR_USERNAME.github.io/teppeki-quiz/**

> `YOUR_USERNAME` はご自身の GitHub ユーザー名に置き換えてください。
> リポジトリ名を `teppeki-quiz` 以外にした場合は、URL の末尾もそのリポジトリ名に変えてください。

## 📁 フォルダ構成

```
teppeki-quiz/
├── index.html   # テスト本体（これが Pages で表示されます）
├── .nojekyll    # Jekyll の処理を無効化して、そのまま表示させるための空ファイル
└── README.md    # このファイル
```

## 🚀 公開手順

1. GitHub で新しいリポジトリ `teppeki-quiz` を作成します（Public）。
2. このフォルダの中身をプッシュします。

   ```bash
   cd teppeki-quiz
   git init
   git add .
   git commit -m "Add vocabulary quiz"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/teppeki-quiz.git
   git push -u origin main
   ```

3. リポジトリの **Settings → Pages** を開きます。
4. **Build and deployment** の Source で **Deploy from a branch** を選びます。
5. Branch を **main**、フォルダを **/ (root)** にして **Save** を押します。
6. 1〜2分待つと、上記のリンクでテストが表示されます。

## ✏️ 問題の追加・編集

`index.html` の中の `QUESTIONS` 配列に、次の形式で問題を追加してください。

```js
{
  ja: "日本語訳",
  pos: "形容詞",              // 問題文に出る品詞・形のヒント
  en: "英文（空欄は (   ) ）",
  choices: ["A", "B", "C", "D"],
  answer: 1,                  // 正解の番号（0 = A, 1 = B, 2 = C, 3 = D）
  why: "正解の理由",
  others: ["他の選択肢が合わない理由", "..."]
}
```
