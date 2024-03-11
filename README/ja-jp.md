# Extended Strings

Extended Strings（拡張文字列）リソース パックは、デフォルトで不足している文字列を補充したり、コマンドなどでよく使われそうな文字列を追加したりします。

## 追加される文字列

* XI（11）から CCLV（255）までのエンチャント レベル用のローマ数字（キーはビルトインのスタイルに基づく）
* 「1 日」、「2 週間」、「3 か月」などの時間の単位（一部のキーはビルトインのスタイルに基づく）
* レコードの作曲者名
* 「緑色のリンゴ」、「緑色の松明」、「赤紫色の松明」などのカスタム色付きアイテム用の文字列
* 「耐火のリンゴ」、「ありふれたニンジン」、「俊敏のパン」などのカスタム効能付きアイテム用の文字列
* カスタム スポーン エッグ用の文字列「%s のスポーン エッグ」
* 「攻撃したとき:」、「使用したとき:」
* I（1）と VII（7）から CCLVI（256）までのステータス効果レベル用のローマ数字（キーはビルトインのスタイルに基づく）
* 「追加」、「適用」、「閉じる」
* 「コピー」、「貼り付け」、「切り取り」
* カスタム キーボード ショートカット用の文字列「%s + %s」
* 「詳細」、「保存」、「検索」、「並べ替え（Sort）」、「並べ替え（Sort by）」
* 時間の前後を示す文字列「%s 前」と「%s 後」
* 「数秒」
* 「晴れ」、「雨」、「豪雨」

追加される文字列については、[ソース コード](https://github.com/myhttps/extended-strings/blob/main/assets/minecraft/lang/ja_jp.json)をご覧ください。

## 文字列の使い方

「検索」と表示するときに、次のコマンドが使われることがあります:

```
/tellraw @s "検索"
/tellraw @s {"text":"検索"}
```

**結果:** 日本語: `検索`、英語: `検索`、リソース パックを使用していないとき: `検索`

---

文字列を使って「検索（`text.type.search`）」と表示するには、次のコマンドを使用します:

```
/tellraw @s {"translate":"text.type.search","fallback":"Search"}
```

**結果:** 日本語: `検索`、英語: `Search`、リソース パックを使用していないとき: `Search`

---

「%s 前（`text.type.time.ago`）」の %s に「数秒（`text.type.time.few`）」を挿入するには、次のコマンドを使用します:

```
/tellraw @s {"translate":"text.type.time.ago","fallback":"%s ago","with":[{"translate":"text.type.time.few","fallback":"A few seconds"}]}
```

**結果:** 日本語: `数秒前`、英語: `A few seconds ago`、リソース パックを使用していないとき: `A few seconds ago`

## 翻訳

[Crowdin](https://crowdin.com/project/extended-strings) に参加して、Extended Strings の翻訳にご協力ください！
