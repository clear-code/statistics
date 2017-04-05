# アップストリームへのフィードバック

アップストリームへのフィードバックの記録である。

## データ

月毎にCSVファイルを作る。例えば、次の通りである。

  * `2017-04.csv`: 2017年4月分
  * `2017-05.csv`: 2017年5月分

CSVのフィールドは左から順に次のとおりとする。

| 項目名 | 例  | 説明 |
| ------ | --- | ---- |
| 日付   | `2017-04-01` | フィードバックした日。[ISO 8601形式](https://ja.wikipedia.org/wiki/ISO_8601) |
| ユーザーID | `kou` | 全データを通じて一意に同一人物を特定でき、わかりやすいもの |
| アップストリームID | `arrow` | 全データを通じて一意に同一プロジェクトを特定でき、わかりやすいもの。 |
| フィードバック種類 | `patch` | パッチを（pull requestとかで）フィードバックした場合は`patch`、バグレポートや機能提案などは`report`、有用な情報の提供は`info`とする。今後増えるかも。 |
| URL | `https://github.com/apache/arrow/pull/481` | フィードバック内容を確認できるURL |

例：

```csv
2017-04-02,kou,arrow,patch,https://github.com/apache/arrow/pull/480
2017-04-04,kou,parquet-cpp,info,https://github.com/apache/parquet-cpp/pull/290#issuecomment-291356052
```
