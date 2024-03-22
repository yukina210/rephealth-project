# rephealth-project

### サービス概要
- 爬虫類飼育者のユーザーが、飼育している爬虫類の健康管理・記録を行える。
- 質問掲示板があり、飼育者同士で問題解決ができる。

### このサービスへの思い・作りたい理由
私自身、爬虫類を飼育しており、爬虫類飼育者のコミュニティでは多くの飼育者が複数匹・複数種飼育していることがわかった。
爬虫類は同じ蛇でも好みの餌が違っていたり、次の食事までの期間が数日単位の種類から月単位と種類によって大きく変わり、その中で拒食してしまう個体がいたり、冬眠させる飼育者がいたりと、飼育頭数や種類が増える毎に管理も複雑になるため、それを解決するアプリを作りたかった。
また、元々動物病院併設のペットショップで勤務していた経験から、多くのペットが飼い主の数字による管理不足が原因で不調に気づかず亡くなる現場を経験してきたため、「記録」する大切さを多くのペット飼育者に広めたいと思っていた。

### ユーザー層について
爬虫類愛好家やエキゾチックアニマルショップなど、爬虫類を飼育している個人や団体が対象。
中でも、ペットの健康管理を重視し、正確な記録を取りたいと考えている層。

### サービスの利用イメージ
ユーザーはアプリにログインし、飼育している爬虫類を登録します。登録後、各ペットの体重記録や、食べた餌の種類や量、排泄の記録を行うことができる。これにより、健康状態のトラッキングや飼育環境の最適化が可能となり、不調や変化に気づきやすくなる。ペットの不調で動物病院へ行った際も、体調の変化を正確に伝えることができる。
また、飼育方法や体調について質問・回答でき、ユーザー同士のコミュニティで助け合うことができる。

### ユーザーの獲得について
- SNSでの情報発信：YouTubeで爬虫類飼育者インフルエンサーや獣医師とコラボレーションを行う。
- コミュニティイベントへの参加：爬虫類展示即売会などへの出展。

### サービスの差別化ポイント・推しポイント
差別化ポイント：爬虫類に特化した健康管理機能とコミュニティサポート。

### 機能候補
- ユーザー登録
- ペットの登録機能（ステップ入力・確認画面を使用）（名前・雌雄・月齢・種類・よくあげる餌など）
- 体重記録（グラフ表示）
- 給餌記録（カレンダー表示）
- 排泄記録（カレンダー表示）
- 脱皮記録（カレンダー表示）
- 産卵記録（カレンダー表記）
- 質問投稿機能（ユーザー）
- 質問回答機能（ユーザー）
- 回答評価機能（ユーザー）
- 質問検索機能（マルチ検索・オートコンプリートを使用）

### 追加機能の案
- 鳥類、哺乳類など記録できる動物の追加
- 記事投稿機能（管理者のみ）
- 記録データを元に幼体期の平均成長曲線や、種類毎の平均体重、給餌頻度などのデータ記事作成（管理者のみ）
- 広告表示機能

### 機能の実装方針予定
- OAuth認証API（ユーザー登録）
- Stimulus Autocomplete（Rails7 ）（検索機能）
- JQuery（検索機能）
- マルチステップフォーム（ペットの登録）
- simple_calender(給餌、排泄、脱皮、産卵記録）
- chartkick（体重推移表示)
- AWS（データベース）

### 使用技術スタック
#### バックエンド
- Ruby on Rails: バックエンドの開発に使用します。データモデルの設計やAPIエンドポイントの作成に活用。
- OAuth認証API: ユーザー登録やログインにOAuth認証を使用。

#### フロントエンド
- HTML, CSS, JavaScript: フロントエンドの実装に使用します。ユーザーインターフェースやクライアントサイドの処理を構築。
- Stimulus Autocomplete: 検索機能にAutocomplete機能を実装。
- JQuery: 検索機能にJQueryを活用。

#### データベース
- AWS: データベースとしてAWSを使用。

#### その他ツール・ライブラリ
- simple_calendar: カレンダー表示にsimple_calendarを導入。給餌、排泄、脱皮、産卵などの記録を視覚的に管理。
- chartkick: 体重推移をグラフ表示するためにchartkickを利用。ペットの健康状態を視覚的に把握しやすくする。