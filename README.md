test
====

test

説明用Gitリポジトリ

## 注意点
* .gitignoreを固定させ、個人のローカル情報をコミットしないようにする
* コミットする際のコメントに何を実装しているのかを記す
* 常にpull requestでプッシュしておく→ソースレビューは他の人が問題なければOKとする
* 

## ソースレビュー

### なぜするか
* バグ、脆弱性の早期発見

### なにを見るか
* 命名規則→基本は、名前はGoogle翻訳でよさ気なのを使うこと。(x kensaku(), o search())
* コメントは最小限に。コメントを書かないと理解できないソースがゴミ。多少わかりづらいところなら仕方ないが、各メソッド内に20％以下に留める。何をしているかは、Javadocに書けばいい。
* 設計の不自然さ→継承、インタフェース、委譲、unsafeなどは最低限
* パフォーマンス→無駄な処理が多くないかどうか。インスタンスをやたらと作りすぎてないか。特にネイティブなので、メモリにダメージを与えないような実装をしたい。
* メモリ開放→マジで死ぬやつ
* 再起→これも死ぬやつ
* 境界値テスト
 
## Gitフロー（1～3名）
* developで開発する
* リリースのタイミングでmasterにマージ
* 緊急的なのは、hotfixで対応する
 
## 開発環境
* OS => Linux or Mac
* Java => 1.7
* Gradle => 2.1
* Android Studio => 0.8.6
* Android OS => 4.4
* GenyMotion(実機ないなら)
