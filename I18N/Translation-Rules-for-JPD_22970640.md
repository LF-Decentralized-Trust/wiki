1. [I18n](index.html)
2. [International groups](International-groups_22970373.html)
3. [Japanese Documentation Working Group](Japanese-Documentation-Working-Group_22970444.html)

# I18n : Translation Rules for JPD

Created by Satomi Tsujita, last modified by Tatsuya Sato on Aug 31, 2021

- [Translation Flow](#TranslationRulesforJPD-TranslationFlow)
- [Project Management](#TranslationRulesforJPD-ProjectManagement)
- [翻訳範囲](#TranslationRulesforJPD-%E7%BF%BB%E8%A8%B3%E7%AF%84%E5%9B%B2)
- [日本語文章統一ルール](#TranslationRulesforJPD-%E6%97%A5%E6%9C%AC%E8%AA%9E%E6%96%87%E7%AB%A0%E7%B5%B1%E4%B8%80%E3%83%AB%E3%83%BC%E3%83%AB)
- [Issue/Pull Request発行](#TranslationRulesforJPD-Issue/PullRequest%E7%99%BA%E8%A1%8C)
- [PR投稿前のセルフチェックリスト](#TranslationRulesforJPD-PR%E6%8A%95%E7%A8%BF%E5%89%8D%E3%81%AE%E3%82%BB%E3%83%AB%E3%83%95%E3%83%81%E3%82%A7%E3%83%83%E3%82%AF%E3%83%AA%E3%82%B9%E3%83%88)
- [本家から引き継いでいるWARNING一覧](#TranslationRulesforJPD-%E6%9C%AC%E5%AE%B6%E3%81%8B%E3%82%89%E5%BC%95%E3%81%8D%E7%B6%99%E3%81%84%E3%81%A7%E3%81%84%E3%82%8BWARNING%E4%B8%80%E8%A6%A7)
- [最新の本家ドキュメントパッチの取り込み方法](#TranslationRulesforJPD-%E6%9C%80%E6%96%B0%E3%81%AE%E6%9C%AC%E5%AE%B6%E3%83%89%E3%82%AD%E3%83%A5%E3%83%A1%E3%83%B3%E3%83%88%E3%83%91%E3%83%83%E3%83%81%E3%81%AE%E5%8F%96%E3%82%8A%E8%BE%BC%E3%81%BF%E6%96%B9%E6%B3%95)
  
  - [取り込み方法](#TranslationRulesforJPD-%E5%8F%96%E3%82%8A%E8%BE%BC%E3%81%BF%E6%96%B9%E6%B3%95)
    
    - [本家ドキュメント更新を取り込んだパッチのコミットメッセージのフォーマット](#TranslationRulesforJPD-%E6%9C%AC%E5%AE%B6%E3%83%89%E3%82%AD%E3%83%A5%E3%83%A1%E3%83%B3%E3%83%88%E6%9B%B4%E6%96%B0%E3%82%92%E5%8F%96%E3%82%8A%E8%BE%BC%E3%82%93%E3%81%A0%E3%83%91%E3%83%83%E3%83%81%E3%81%AE%E3%82%B3%E3%83%9F%E3%83%83%E3%83%88%E3%83%A1%E3%83%83%E3%82%BB%E3%83%BC%E3%82%B8%E3%81%AE%E3%83%95%E3%82%A9%E3%83%BC%E3%83%9E%E3%83%83%E3%83%88)
  - [本家ドキュメント更新のウォッチ方法や取り込みタイミング](#TranslationRulesforJPD-%E6%9C%AC%E5%AE%B6%E3%83%89%E3%82%AD%E3%83%A5%E3%83%A1%E3%83%B3%E3%83%88%E6%9B%B4%E6%96%B0%E3%81%AE%E3%82%A6%E3%82%A9%E3%83%83%E3%83%81%E6%96%B9%E6%B3%95%E3%82%84%E5%8F%96%E3%82%8A%E8%BE%BC%E3%81%BF%E3%82%BF%E3%82%A4%E3%83%9F%E3%83%B3%E3%82%B0)
- [Translation tools](#TranslationRulesforJPD-Translationtools)
- [翻訳・対訳集 サブグループ](#TranslationRulesforJPD-%E7%BF%BB%E8%A8%B3%E3%83%BB%E5%AF%BE%E8%A8%B3%E9%9B%86%E3%82%B5%E3%83%96%E3%82%B0%E3%83%AB%E3%83%BC%E3%83%97)
  
  - [Scope: 目的](#TranslationRulesforJPD-Scope:%E7%9B%AE%E7%9A%84)
  - [Members](#TranslationRulesforJPD-Members)

翻訳の過程で蓄積されていくテクニックや予めルール／方針を統一しておいた方が手間がかからなくて皆が幸せになるような事項を以下にまとめる。

## **Translation Flow**

This slide show a draft.

翻訳フローのオレンジ色の部分を現在議論中です。こちらのスライドはドラフトです。

また、zoomミーティングで下記フローを実際に実行しながら確認したときのビデオが[2020 08 04 JPDWG Agenda](2020-08-04-JPDWG-Agenda_22970632.html)にありますので、ご参考いただければ幸いです。もし、翻訳以外の部分（ツールの使い方、コマンド、インストールなど）でお困りのことがありましたら、Membersテーブルの"technical support : yes"の方または、チャットへお気軽にお問い合わせください。

[![](attachments/thumbnails/22970444/22971341)](attachments/22970444/22971341.pptx)

## **Project Management**

We use GitHub issues, projects, and milestone for project management.

Githubのissueで翻訳する旨のコメントをお願いいたします。もし、翻訳着手されていないissueがあれば、そちらを担当いただいてもOKです。

issueには、下記の内容を含めて設定ください。例：[https://github.com/hyperledger/fabric-docs-i18n/issues/116](https://github.com/hyperledger/fabric-docs-i18n/issues/116)

- タイトル：翻訳するドキュメントの階層
- 詳細：readthedocの該当ページと翻訳ファイルのURL
- Assignees：翻訳する方のアカウント
- Labels：jaJP-docs-ongoing
- Projects：ja-JP

既存のissueに関しては、Assigneesが未設定、かつ、コメント欄で誰も担当することを宣言していない、場合には翻訳未着手とみなすこととします。

翻訳未着手のissueを担当したい場合には、そのissueのコメントにて自分が担当する旨記載してください  
(※Assigneesの設定はmaintainerしか設定できないためOptionalとします)。

Githubのマイルストーンは今後必要に応じて設定します。

また、翻訳着手されましたら、下記のプロジェクトページのカードを"In progress"に移してください。

[https://github.com/hyperledger/fabric-docs-i18n/projects/1](https://github.com/hyperledger/fabric-docs-i18n/projects/1)

## **翻訳範囲**

概要種別説明例(File/Issue/Pull Request)備考

Status

(Draft/Approved)

ヘッダは訳さなくてもよいmd

ページ内に目次を置く場合、アンカーの都合上、英語のままの方が手間がかからない。

和訳した各ヘッダーにリンク張るためには少しトリッキーな方法が必要だった。

[international\_languages.md](https://github.com/hyperledger/fabric-docs-i18n/blob/52666f25a6e448c9cea1e5861108d308a3e64478/docs/locale/ja_JP/source/international_languages.md)

※特に決定事項というわけでもなさそうなので後ほどでご意見お聞かせください（チャットもしくはミーティングで）

※rstも同じかもしれません

Approved(2020/08/18)

ヘッダは訳さなくてもよい

rst

特にトリッキーなことをせずに日本語に変換できる場合は、分かりやすさを優先して翻訳する

Approved(2020/08/18)  
共通

rst

## **日本語文章統一ルール**

表記ゆれを防ぐために本WGが定める基本的な日本語文章のルールです。

概要備考

Status

(Draft/Approved)

語尾は「である」調ではなく「ですます」調を使う  
Approved句読点は「，」「．」ではなく「、」「。」を使う  
Approved

## **Issue/Pull Request発行**

概要説明例(File/Issue/Pull Request)

Status

(Draft/Approved)

コミットメッセージおよびPRのタイトルは“\[ja\_JP]” で始める 

ログや一覧で見分けやすいように

[\[ja\_JP\] translate glossary.rst into Japanese · hyperledger/fabric-docs-i18n@127a41d](https://github.com/hyperledger/fabric-docs-i18n/commit/127a41d9c2de7fcc4b8acc6fbd90da6d25ca7875#diff-07a2e8a04a76b2c18e93d8aecad07ea2)

[\[ja\_JP\] translate glossary.rst into Japanese by Naoya-Horiguchi · Pull Request #62 · hyperledger/fabric-docs-i18n](https://github.com/hyperledger/fabric-docs-i18n/pull/62)

Approved(2020/08/18)Issue/PRのタイトルはファイル名よりもドキュメントの階層を明記するその方が実際のドキュメント構成とのマッピングがしやすく抜け漏れの確認も楽になるKey Concepts &gt;&gt; Fabric chaincode lifecycle Approved(2020/09/01)

## **PR投稿前のセルフチェックリスト**

概要説明備考

Status

(Draft/Approved)

Translation Rulesに従っているか本ページのセクション全体を確認してください。  
Approved(2020/08/18)Hyperledger Fabric固有の単語に関して用語集に従っているか[https://github.com/linuxfoundation-jp/HL\_Fabric\_Doc-Jp](https://github.com/linuxfoundation-jp/HL_Fabric_Doc-Jp)  
Approved(2020/08/18)

ドキュメントビルド時(make html)に、

追加のWARNINGメッセージが出ていないことを確認する

自身の編集作業によって新たに発生したWARNINGはできる限り無くなるように対応してください。

　- WARNINGを確認することで、特にrstファイルについて、デッドリンク含めたフォーマットミスはある程度気付くことができます。

　- 些細なものもありますが全体数を増やさないことが、他のコントリビュータが自身の追加したWARNINGに気付くのを助け、全体の品質維持につながります。

**※注意事項:** 数件のWARNINGは本家から引き継いで発生していますので（後述のWARNING一覧参照）、これらは無視してください。

Approved(2020/08/18)

ビルド後に、自身が翻訳したページについてブラウザ等で参照し、

フォーマット崩れがないことを一通り確認する

- rst 形式の場合、インラインマークアップの前後に全角文字が隣接する場合、空白を入れる必要がありますが、それが漏れてフォーマットが崩れてしまうことがよくあります。
- markdown 形式の場合、全角文字が隣接していてもきちんとマークアップされるようです (「あああ\*\*強調\*\*いいい」などでよいです)。

<!--THE END-->

- 文章中のリンク箇所については一通り実際にリンク先への遷移まで確認することが望ましいです。

Approved(2020/08/18)

1ファイルの翻訳につき1 commitとなっていること

レビューを受けて修正した場合でも、原則的にcommitは1つにまとめる。複数ファイルを翻訳した場合には、ファイルごとに別commitとする。

ただし、同様の修正を複数のファイルにわたって行う場合 (アンカーの修正など) などはこの限りでない。

Approved(2020/08/18)

## **本家から引き継いでいるWARNING一覧**

release-2.2においては、本家から引き継いで以下のchecking consistency WARNINGが発生しています（2020年8月13日時点）。これらはどこからもリンクが張られていないために発生している警告となります。

日本語翻訳時には、これらは警告については無視してください。

- source/build\_network.rst: WARNING: document isn't included in any toctree
- source/developapps/[apis.md](http://apis.md): WARNING: document isn't included in any toctree
- source/github/github.rst: WARNING: document isn't included in any toctree
- source/ledger.rst: WARNING: document isn't included in any toctree
- source/msp-identity-validity-rules.rst: WARNING: document isn't included in any toctree
- source/policies.rst: WARNING: document isn't included in any toctree
- source/security\_model.rst: WARNING: document isn't included in any toctree
- source/tutorial/[installxcode.md](http://installxcode.md): WARNING: document isn't included in any toctree

## **最新の本家ドキュメントパッチの取り込み方法**

本家最新ドキュメントとの更新差分を翻訳プロジェクトのほうに取り込む方法とその運用ポリシーは以下のとおりとする。

##### 取り込み方法

- 本家(release-2.2ブランチ)のドキュメント更新パッチ1件ごとにそのパッチを適応した翻訳パッチも1件とする。
  
  - 未翻訳の新しいファイルの場合には良い機会なので翻訳も実施する。
- コミットメッセージには、**下記フォーマットに従って、取り込んだ本家ドキュメント更新コミットのコミット番号を必ず記載すること**。

###### 本家ドキュメント更新を取り込んだパッチのコミットメッセージのフォーマット

\-------------------------

```sh
[ja_JP] Sync with release-2.2 (translated)

commit: 9a6b35104e88dc2df08db7c7b0ba3d0f61127a85
```

\-------------------------

##### 本家ドキュメント更新のウォッチ方法や取り込みタイミング

- **基本的には、マイナーリリースのタイミングでチェックして実行する****。**
- ただし、個々人でやりたい人は都度対応してもよい。
- 上記での抜け漏れやその対応状況も確認するために、取り込みパッチにはフォーマットに従って本家のコミット番号を必ず付与すること。

## **Translation tools**

みんなの自動翻訳 TexTra（このツールの使用は必須ではありません。）

[https://mt-auto-minhon-mlt.ucri.jgn-x.jp](https://mt-auto-minhon-mlt.ucri.jgn-x.jp)

翻訳にあたっては、下記の用語、対訳データを参考に翻訳をお願いいたします。

[https://github.com/linuxfoundation-jp/HL\_Fabric\_Doc-Jp](https://github.com/linuxfoundation-jp/HL_Fabric_Doc-Jp)

## **翻訳・対訳集 サブグループ**

#### Scope: 目的

1\. Hyperledger Fabricの英語ドキュメントを日本語へ翻訳する際に使用する専門用語や表現の共有

2\. translator/reviewerのサポート

3\. TexTraとの連携

#### Members

Emi MaekawaSatomi TsujitaTaku ShimosawaTatsuya SatoYuki Kondo

Document generated by Confluence on Nov 26, 2024 16:47

[Atlassian](http://www.atlassian.com/)
