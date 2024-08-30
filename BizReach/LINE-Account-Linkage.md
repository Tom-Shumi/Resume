# LINE 連携機能開発プロジェクト

## 役割

- リードバックエンドエンジニア

## 使用技術

- Typescript
- Node.js
- AWS Lambda
- Java
- Spring Boot
- Terraform
- Github Actions

## プロジェクト期間

- 半年

## 開発手法

アジャイル（スクラム）

## プロジェクト概要

自社で運営しているサービスのアカウントとユーザの持つ LINE アカウントを連携して、自社サービスからユーザに PUSH している情報を LINE でも受け取れるようにする。

## 担当

- 上記の開発案件のバックエンドエンジニアとして API・基盤開発を行いました。
- 工程としては、要件定義〜運用保守まで担当しました。
- プロジェクトマネージャーとして、メンバー 4 人の進捗管理や他チームとの調整を行いました。

## 開発

### アーキテクチャ設計

LINE アプリを用いたサービスを開発するのが自社プロダクト内で初めてだったので、テックリード的な立場であった自分がドキュメントを読み漁り LINE 社が提供している API 仕様を理解しました。

その後アーキテクチャ設計を行ない、AWS 上でどうすれば本プロジェクトでやりたいことが実現できるのかインフラチームも巻き込みながら決定していきました。
（その際に私の方で、「アーキテクチャ図」、「LINE アカウント連携までのシーケンス図」を作成して、他者が理解できるように説明を行いました。）

**◼︎ 検討し、意思決定したもの**

- 使用する DB（RDS or DynamoDB or Redis etc...）
- API gateway の種類（REST API or HTTP API）
- LINE 社からの Webhook 受け取る API の技術スタック（Lambda or ECS）（Javascript or Java or Python）

作成したアーキテクチャ設計に従い、実際に私の方で Terraform を使い AWS リソースの定義を記述し、本番にデプロイしています。

## 進捗管理

本プロジェクトは、既存プロダクトの保守運用と並行して開発を行なっていたため、障害対応や法令・脆弱性対応などの割り込みタスクと並行して開発を進める必要がありました。

プロジェクトマネージャーだった私の方で本プロジェクトの残タスクを整理して、「この開発速度だといつまでにリリースができるか」を常に見える化し、プロダクトマネージャやプロダクトオーナーと他タスクの優先順位を比較できる状態を作りました。

結果、当初予定していたスケジュール通りには行きませんでしたが、ステークホルダーとスケジュール・進捗について定期的に合意が取れていたので、スケジュール遅れについても大きな影響がなくプロジェクトを完了することができました。