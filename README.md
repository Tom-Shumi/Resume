# 職務経歴
## 1.商品販売アプリ
#### ●プロジェクト概要
ユーザがギフト（商品）の送受信を行える、某大手SNS企業が運営するtoC向けのスマホアプリの開発。

#### ●期間
2021年4月〜現在

#### ●使用技術
Java, Spring boot, Perl, Linux, Docker, MySQL, Redis, Elasticsearch, Docker, Drone

#### ●開発手法
アジャイル（スクラム）

#### ●担当業務
上記の開発案件のバックエンドエンジニアとしてAPI開発を行なっています。  
工程としては、要件定義〜UTを担当し、部下3名のチームリーダーとして、マネジメントも行っています。

#### ●API開発
直近の案件ではHome画面の改善を行いました。

Home画面の表示に時間がかかるという企画チームからの課題に対して、APIのレスポンスを速くすると共に、表示するコンテンツについても刷新しようという要件でした。

上記の課題を解決するために、まずHome画面の表示に使用するAPIを分割するという設計を提案しました。  
既存では一つのAPIでHome画面に表示するコンテンツを全て取得しており、そのAPIに時間がかかっていたので、APIを複数に分割してフロントエンドから複数回APIを実行する方針に変更しました。  
Home画面の下部に表示するコンテンツは、レスポンスが多少遅れても問題ないため、上記案で設計しAPIを開発することで、課題を解決する事ができました。

また上記の開発時に、一度取得したコンテンツをキャッシュしておくRedisサーバとの連携も必要になったため、その接続部分やインターフェース周りの実装も私が担当しました。

#### ●Java化
本スマホアプリのバックエンドは元々Perlで書かれていたのですが、現在はそのPerlのコードをJava化する案件も並行して走っています。上記HOME画面の改善を行う前はJava化案件の方にアサインされていました。

私のチームではメンバー全員がこれまでPerlを触ったことがなく、Perl自体も他言語ではあまり見ない記号を用いた癖のある記述ができるため、キャッチアップしていくのにかなり苦労しました。

いち早くキャッチアップするための取り組みとして、Perl辞書の作成をしました。  
メンバーそれぞれが調査して分かったPerlの書き方を都度wikiの一覧にまとめて、デイリースクラム後に時間を取り、そのナレッジを共有する場を設けました。  
上記の取り組みのおかげで、メンバー全員のPerlに対する知識が底上げされ、今では何のストレスもなくPerlコードが読み書きできるようになりました。

私自身がJVM系の言語ばかり使用しており、それ以外の言語に対して少し壁のようなものを感じていましたが、本案件を通して他の言語でもキャッチアップして行ける自信をつけることができました。

## 2.ラジオ配信アプリ
#### ●プロジェクト概要
某大手SNS企業がリリースする予定だったラジオ（トーク）配信アプリのバックエンド開発に立ち上げから参画しました。  
ラジオ版のYouTubeがテーマになっており、配信者が自由に自身のラジオを配信できるサービスです。

開発が始まって2ヶ月が経過した頃、他社から「Clubhouse」がリリースされたため、差別化が図れず途中でプロジェクトは凍結となりました。

#### ●期間
2021年1月〜2021年3月

#### ●使用技術
Kotlin, Spring boot, Linux, Docker, MySQL, Redis, Docker, Drone

#### ●開発手法
アジャイル（スクラム）

#### ●担当業務
上記の開発案件のバックエンドエンジニアとしてAPI開発を行なっていました。  
工程としては、設計〜UTを担当しており、DBの論理設計も行いました。

#### ●DB論理設計
要件定義書や画面イメージ等をインプットに、テーブル名・カラム名・カラムの型・主キーやインデックス等を設計し、ER図も作成しました。  テーブル数は、アプリケーション全体で30個ほどになりました。

論理設計をする際は正規化を意識して、同じ情報を複数のテーブルで保持しない様にすることはもちろんのこと、「性能を良くするため」や「ログ管理のため」にあえて正規化をしないなど、実装を意識したテーブル設計を行いました。

またわかりやすく、正しい意図で伝わるように具体的で統一感のあるカラム名・テーブル名を意識し命名しました。  
・idやflg、statusが何を指しているのか明確にする。  
・プレフィックスをつけてカテゴライズし、用途をわかりやすくする。  
・「その他」カラムなどを使わない。  

## 3.遺伝子情報管理システム
#### ●プロジェクト概要
ユーザの遺伝子情報の管理を行うWebアプリケーションの開発。

健診の際に行う血液検査で採取した血液を用いて、遺伝子情報の解析を行うサービス。  
遺伝子情報の解析自体は別システムが行い、私は解析した遺伝子情報の管理とユーザへの公開を行うシステムの開発を行いました。

#### ●期間
2020年1月〜2020年12月

#### ●使用技術
Java, Spring boot, Thymeleaf, Bootstrap, Javascript, CSS, SQLServer, WindowsServer

#### ●開発手法
ウォーターフォール

#### ●担当業務
上記の開発案件に立ち上げから携わり、要件定義～リリース、運用保守の工程を担当していました。  
また部下6名のチームリーダーとして、マネジメントも行っていました。

#### ●アプリケーション開発
立ち上げから参画していたため、実装面ではAP基盤の部分を主に任されており、Spring Securityを用いた認証処理やログ出力、共通的なエラー処理を主に担当していました。

遺伝子情報という機微な個人情報を扱うシステムということもあり、セキュリティ要件や管理者の権限の持ち方が複雑だったためSpring Securityの機能をそのまま使用するのではなく、データベースに機能ロール（どの操作ができるのか）と集合ロール（どの情報にアクセスできるのか）という概念を定義し、柔軟に権限管理ができるように設計・実装を行いました。

AP基盤部分の実装後は、主に上流工程（要件定義や設計）を担当しており、実装部分はほとんど行なっていませんでした。

#### ●要件定義
本プロジェクトでは業務要件をまとめるのにとても苦労しました。  
顧客からいただく情報が全て、機能要件レベルまで落とし込まれた情報だったため、一番肝心の「なぜその機能が必要なのか」の部分が抜けていたためです。

なので第一優先として業務フローを作成することに注力しました。  
顧客にヒアリングし大まかな業務フローを作成し、そこからまた課題・不明点を洗い出して再度ヒアリングして。。ということを何度も行い、その中で業務フローをブラッシュアップしていきました。  
そのおかげもあって、「なぜその機能が必要なのか」の部分を明確にすることができました。  
機能要件もより正確なものに仕上げることができ、過不足もはっきりし、設計以降のフェーズをスムーズに行うことができました。

#### ●マネジメント
本プロジェクトでは部下6名のマネジメント・教育を行いながら実務も担当していました。  
タスクの割り振りや、スケジュール遅延時のリカバリ案の検討など、実務と並行で行うのは大変でしたが、リーダーである私が「タスクを抱え込みすぎて機能していない」というような状態にならないために、メンバーに振れるタスクはメンバーに適切に振って、チーム全体を俯瞰して見るように心がけていました。

またリーダーとして顧客折衝も担当していました。  
四半期に一度リリースをしていたのですが、顧客からの要求が毎回こちらの予算内には収まりませんでした。  
その都度、業務フローの明確化・要求の優先順位の整理を行い、開発スコープの調整を顧客と行っていました。

上記の対応もあり、厳しいスケジュールの中でしたが、毎回期日通りにリリースを行うことができていました。

## 4.健康管理システム
#### ●プロジェクト概要
企業に所属する社員の健康診断の結果の管理や、ストレスチェックアンケートの実施等を行うWEBアプリケーションの開発。

#### ●期間
2015年7月〜2019年12月

#### ●使用技術
Java, Struts, Spring Framework, JSP, Javascript, CSS, Oracle, Linux, WindowsServer

#### ●開発手法
ウォーターフォール

#### ●担当業務
上記の開発案件の要件定義～リリース、運用保守の工程を担当していました。  
メンバーとして3年間、部下2名のチームリーダーとして1年間、本プロジェクトに従事していました。

#### ●開発工程の効率化
本プロジェクトでの実績としましては、開発工程の効率化を行いました。  

主な取り組みとしましては、ソースコードの品質をあげるため、ソースレビュー実施の前に行うチェックシートの作成や、単体試験仕様書の観点一覧を作成しました。  
また要件定義で決めておかなければならない項目が明確になるよう、要件定義書のフォーマットも作成し、要件定義工程での手戻りや検討漏れを抑制しました。  

上記の取り組みにより、品質向上、レビュー時間の削減、要件定義以降のフェーズのスムーズな進行に貢献しました。
