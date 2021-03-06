## Database > EasyCache > リリースノート

### 2021. 02. 23.

#### 機能改善/変更

* 読み取り専用ドメインのツールチップ追加

#### バグ修正

* プロフィール最大入力値を入力すると、レプリケーショングループが作成されない現象を修正

### 2021. 01. 26.

#### 機能改善/変更

* Maxmemoryデフォルト値を可用メモリの70%から50%に変更
* プロフィールに`activedefrag`関連項目を追加
* **ログ表示** ダイアログボックスUIを改善

#### バグ修正

* モニタリングで時間を変更すると日付が1月2日に変更される現象を修正

### 2020. 12. 29.

#### 機能追加

* 読み取り専用ドメイン機能を追加

#### 機能改善/変更

* 接続制御情報に関連する機能を改善
* インスタンスタイプ変更ボタンにマウスオーバーすると、案内事項が表示されるように改善
* ダイアログボックスのボタン名をOKから確認に修正

#### バグ修正

* レプリケーショングループのプロフィール変更中に変更前のプロフィールを修正すると、プロフィールの修正に失敗して利用不可になる現象を修正
* Webサイトの言語を「日本語」に設定した時、モニタリングフィルタオプションが韓国語表記になっていました。日本語で表示されるように修正しました。

### 2020. 11. 24.

#### 機能改善/変更

* ログ全体画面表示を追加

### 2020.10.27.

#### バグ修正
* レプリケーショングループの名前を変更し、ノードの名前も変更されたレプリケーショングループの名前が反映されるように修正
* CPU, RAMのクォータを超えた場合のエラーメッセージを修正

### 2020.09.22.

#### 機能改善/変更

* 韓国(坪村)リージョンオープン
* ログ確認機能追加
* VPC Subnetリストを名前順に表示
* サービス利用権限対応

#### バグ修正

* モニタリンググラフの単位を修正 
    * 入力バイト：byte -> bytes/1min
    * 出力バイト：byte -> bytes/1min
    * 毎秒処理したコマンド数： counts/seconds -> count/1sec
* プロフィールを修正する時、修正中のプロフィールを使用しているレプリケーショングループの状態がプロフィール修正中と表示されず、正常と表示される現象

### 2020.08.25.

#### 機能改善/変更

* レプリケーショングループ作成時にRedis接続用のパスワードを設定するかどうかをオプションで選択できるように変更

#### バグ修正

* レプリカノード昇格時のノード昇格完了時点とステータスが一致しない現象を修正

### 2020.07.28.

#### 機能追加

* インスタンスタイプ変更機能追加

#### 機能改善/変更

* サポートされるインスタンスタイプからCompute Optimized削除

#### バグ修正

* モニタリンググラフから接続されたクライアントが累積で表示される現象の修正
* ユーザカスタムプロフィールを使用していたRedis 3.2.12のレプリケーショングループバックアップがらリストアする際、デフォルトプロフィールのレプリケーショングループにリストアされる現象を修正

### 2020.06.23.

#### 機能改善/変更

* CloudTrailサービスにイベント登録

#### バグ修正

* ノードが再起動された場合INFOのレディスのサーバーの稼働時間（uptime\_in\_seconds）が実際よりも9時間加わった値で出力される現象を修正
* 接続情報のタブで、パスワードを確認するために表示のボタンをクリックしても、ノードが障害状態である場合には、パスワードを取得に失敗する現象を修正
* HA再設定のボタンが表示されてHAの再設定を実行したが、失敗する現象を修正
* モニタリング画面の検索期間で指定を選択しても、期間を自由に設定することができない現象を修正

### 2020.05.26.

#### 機能改善/変更

* Redis 5.0 サポート
* プロファイルコピー機能提供
* モニタリングの改善
    * 照会タブをレプリケーショングループの詳細画面から初期画面上部の別個のタブに移動
    * 現在時間ボタンを追加
    * 自動更新チェックボックスを追加
    * レプリケーショングループの選択ドロップダウンを追加
    * 単一のグラフをポップアップで表示して、統計項目と集計期間を選択できるように改善
* プロファイルを作成または変更する際に詳細設定を使用して設定値を修正できるように変更

#### バグ修正

* ノードが追加されたレプリケーショングループの変更後に、ノードを追加していないレプリケーショングループを変更しようとした場合、修正ボタンが無効にされている現象を修正
* モニタリング項目で「接続されたクライアントの数」と「ブロックされたクライアントの数」が累積値で表示されるバグを修正
* プロファイルリストの変更後にプロファイルリストが一部しか表示されない現象を修正
* レプリケーショングループで使用されているプロファイルを変更する場合は、修正後の画面がリロードされない現象を修正

### 2020.04.28.

#### 機能改善

- HA監視設定にヘルスチェック応答時間をユーザが設定できる機能提供
- マスタノード手動昇格の機能提供
- モニタリング項目から照会成功・失敗を累積ではなく時間別表示に変更
- アラームルールにメモリ使用量を%で設定できるように変更

#### バグ修正

- １０分単位でモニタリングのグラフが切れて表示される現象修正
- failover後障害ノードが数秒以内に復旧した場合にレプリケーショングループ、ノードステータスが正常に表示されない現象修正
- ワーニング状態のレプリケーショングループのパスワードを変更可能に修正
- 一部メニューとラベル修正

### 2020. 03. 24.

#### 機能改善

- EasyCache基本設定値の変更（tcp-keepalive[0→300]）

### 2020. 02. 25.

#### 機能改善
- 接続情報を同時に複数個を追加ができるように修正
- SMS内容改善
- 重複されたCIDRを入力した際のメッセージ修正

#### バグ修正
- 大容量データがある際、Replicaノードを追加する場合データの同期化が無限ループが発生する問題を修正
- レプリケーショングループでノードの作成が失敗した際、ノードの一覧で作成中の表示が消えずに表示されている問題を修正

### 2020. 02. 11.

#### 機能改善

- TOAST認証モジュールバージョンアップグレード

#### バグ修正
- レプリケーショングループ作成時に、インターネットゲートウェイを設定をしないユーザーのVPCサブネットを選択した場合、失敗する現象を修正

### 2020. 01. 21.

#### 機能改善

- コンソール画面とイベントのメッセージ日本語対応
- Failover後、ドメイン変更失敗の際イベント登録追加

### 2019. 12. 24.

#### 新規サービスリリース

- TOAST EasyCacheは、Redis(REmote DIctionary Server)をクラウド環境で提供するサービスです。
- 簡単な設定で高可用性(自動HA)のRedisサーバーを使用できます。
- Redis 3.2.12バージョンを提供します。
