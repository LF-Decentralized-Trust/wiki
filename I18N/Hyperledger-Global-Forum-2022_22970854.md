1. [I18n](index.html)
2. [International groups](International-groups_22970373.html)
3. [Japanese Documentation Working Group](Japanese-Documentation-Working-Group_22970444.html)
4. [Meetings by JPDWG](Meetings-by-JPDWG_22970537.html)

# I18n : Hyperledger Global Forum 2022

Created by Yuki Kondo, last modified on Sep 08, 2022

### # Dates to Remember

CFP Opens: Tuesday, March 1, 2022 at 12:00 AM PST  
CFP Closes: Friday, April 29, 2021 at 11:59 PM PDT  
CFP Notifications: Thursday, June 2nd  
Schedule Announcement: Week of June 13  
Presentation Slide Due Date: Friday, September 9, 2022  
Event Dates: Monday, September 12 – Tuesday, September 13

### # SCHED

9/13(Tue) 12:05 - 12:45, [Beyond the Language Barrier – Translating Hyperledger Fabric Documentation Into Japanese](https://hgf22.sched.com/event/14H4H/beyond-the-language-barrier-translating-hyperledger-fabric-documentation-into-japanese-yuki-kondo-hitachi-ltd-daiki-nakashima-mitsubishi-electric-corporation)

### # Call For Proposals (CFP)

[https://events.linuxfoundation.org/hyperledger-global-forum/program/cfp/](https://events.linuxfoundation.org/hyperledger-global-forum/program/cfp/)

\## Type of Submission  
Presentation

\## Abstract Title  
Beyond the language barrier - Translating Hyperledger Fabric Documentation into Japanese

\## Abstract  
Hyperledger Fabric is used for various use cases all over the world. However, it was hard for non-English speakers to learn the technology correctly because the official documentation was written in English and updated quickly. The quick updates made the local language's learning resources outdated soon. To remove the language barrier, Hyperledger Fabric Documentation Working Group started translating the official documentation in various language. When the content is available in the native language, more companies will easily learn and adopt Hyperledger Fabric technologies. As one of the sub-groups, Japanese Doc WG was launched in July 2020. Japanese Doc WG created the translation contribution process, communication channel (e.g. monthly Zoom meeting, Japanese chat group) and Kanban board. To improve the productivity and quality, Japanese Doc WG made Japanese terminology and introduced a translation tool while collaborating with translation experts. Japanese Doc WG also hosted Meetups to increase the number of contributors. In this session, Japanese Documentation WG will share their experiences for other language communities to work on the translation.

\## Session Details  
The purpose of this session is to share the knowledge of translation efforts.  
Japanese Documentation WG will make a presentation with slides to explain the motivation and activities.  
After the presentation, Q&amp;A session continues. There is no demo and interactive contents.

\## Learning Outcomes  
Better understanding of creating a translation working group.  
Tips on translation to keep the quality.  
Tips on review process.

\## Related Activities  
[https://www.meetup.com/ja-JP/Collaborative-Translation-Meetup/events/277408780/](https://www.meetup.com/ja-JP/Collaborative-Translation-Meetup/events/277408780/)  
[https://www.meetup.com/Collaborative-Translation-Meetup/events/281941417/](https://www.meetup.com/Collaborative-Translation-Meetup/events/281941417/)

### # Presentation Slide

日本語WGの経緯や苦労話をリアルなトピックを交えて紹介します。みなさまの経験や意見を募集します。

アイデアのある方は、8月のMontly Meetingまでに書き込みをお願いします。ご協力よろしくお願いします。

大まかなカテゴリを設けたので、Wikiを直接編集してトピックを追加してください。もし、Wikiに書き辛い話題があれば、Chatやメールなどで個別に連絡でも大丈夫です。

⇒ ご協力ありがとうございました。みなさまのおかげで、充実したコンテンツになりました。

#### スライド(完成版, 2022/09/09)

[![](attachments/thumbnails/22970854/22971617)](attachments/22970854/22971617.pptx)

#### WG立ち上げ経緯と苦労話

- 2020.06: 立ち上げ、Fabric Doc WGとのコネクション構築
  
  - HL meetup Kansaiの立ち上げに辻田が関わった関係で、LF Japanが辻田に日本語コミュニティの立ち上げを打診。Davidが翻訳コミュニティを探していたとのこと。
  - LF JapanがDavid Boswell(Community Architect)に、日本語翻訳コミュニティ立ち上げのサポートを依頼。
  - David Boswellの紹介で、Fabric Doc WG Leader(当時) Anthony O'Dowdを紹介してもらう。
  - Fabric Doc WGでは、翻訳活動(Chinese、Malayalam、Portuguese)が始まっていた。日本語は4番目のローカルコミュニティとして活動を開始。
- 2020.06: メンバー募集
  
  - Fabric Doc meeting(6/12)に辻田が出席した際、西島さんと近藤さんが出席されているのを確認し、LF Japanに問い合わせ。
  - LF Japanから日立に声掛け。これ以前に、Fabricの翻訳レビューでLF Japanと繋がりがあった。
  - Anothony(当時 IBM UK)が、IBM Japanのメンバーに声掛け。
  - Japanese Documentation Working GroupのWikiページを立ち上げて、オープンにメンバーを募集。約20人がすぐに参加表明した。
- 2020.06: キックオフミーティング(6/22)
  
  - メンバーの自己紹介、プロジェクトの当面のゴール、日本語用リポジトリのREADME、情報共有方法（wiki、github issueの位置付け）を議論
- 2020.07: コミュニケーションチャネルの確立
  
  - 最初はメンバ同士がメールで直接やり取りをしていて、コミュニケーションが全体に見えないことがネックだった。
  - オープンに議論することで新規メンバが参加しやすいようにしたかった。
  - LFとFabric Doc WGのサポートでコミュニケーションツールを導入した。
  - Japanese Doc WG Chat: WGの開催案内、情報共有、などを日本語でコミュニケーション。
  - 翻訳用リポジトリ: GitHub hyperledger/fabric-docs-i18nに、docs/locale/ja\_JP folderを作成
  - Zoom Meeting: 当初はIBM JapanのアカウントでWebExを設定して、メールで展開していた。運用がクローズになるのを避けるため、LFに相談して、LFのZoomアカウントを利用できるようにしてもらった。
  - Wiki meeting minutes: Meetingの議事録をシェアするためのページを作成。
  - GitHub Kanban: 翻訳作業を可視化するため、GitHubのissueで管理する。他の言語との区別がつくように、jaタグを導入。
- 2020.07-2020.08: 翻訳作業のマイルストーン決定
  
  - 翻訳対象バージョンの決定: 最新のLTSだったv2.2にすることを決定。前世代のLTSであるv1.4の利用者が多かったけれど、将来を見越してv2.2にした。
  - 翻訳ドキュメントの優先順位付け: Fabric Doc WG から提案されたものを採用した。
  - コントリビューションのロール: メンバはFabricの経験値が異なっていた。チーム全体での作業効率を上げるため、翻訳者・レビュア・サポートという区分を設けた。メンバリストで自己申告してもらった。
- 2020.07-2020.09: 翻訳コントリビューション手順の確立
  
  - Fabric Doc WGで、先行して翻訳に取り組んでいた多言語のメンバーAneena(Malayalam)とRenato(Portuguese)からアドバイスをもらいつつ、翻訳コントリビューション手順を作成した。
  - 翻訳ファイルの形式: rstとmdを直接編集する方式を採用。Sphinxの国際化機能([https://www.sphinx-doc.org/ja/master/usage/advanced/intl.html](https://www.sphinx-doc.org/ja/master/usage/advanced/intl.html))を利用する案が提案されたけど、採用を見送った。(理由がうろ覚えなので、追加調査したら追記する。作業が煩雑になり過ぎることを避けたかった？)
  - 翻訳フロー
  - ブランチ戦略
  - レビュー方法
  - LF Japanからの提案で、自動翻訳: みんなの自動翻訳＠TexTraを一部のメンバーで試験導入。
  - 用語の統一を目的に、LF Japanで翻訳したFabricトレーニングコースから用語集を譲り受け、LF JapanのGithub/HL\_Fabric\_Doc-Jpに登録。
  - github Milestonesで進捗管理、まずは優先的に翻訳お願いしたいファイルを設定
  - 日本語グループ向けgithub Labelsを設定
  - ローカルでpull req前のチェックリストほしい =&gt; 知見をwikiに適宜まとめていく
  - 翻訳ルールに追加があった場合は、ミーティングにて意見を募り、プロジェクトのルールとして合意する。
  - 翻訳フローが確立されたので、10月からミーティングを月1回に変更した。それまではBi-Weeklyだった。
- 2020.11 用語集/対訳集のサブグループ立ち上げ
  
  - 用語集/対訳集をTexTraにも対応できる形式で編集し、LF JapanのHL\_Fabric\_Doc-Jpブランチを更新(2021.1~2021.5)
- 2020.11 First goal 100%達成
  
  - 当時、Read the Docへの掲載条件がFirst Goalを達成することだった。
  - LF Staffにお願いして、CIビルドの設定を更新してもらい、日本語DocのRead the Docでの公開を開始。
- 2021.4、2021.11 活動PRのためMeetup開催
- 2021.10 Suggested next topics 翻訳完了

#### コントリビューションプロセスの作成と苦労話

- コントリビューションプロセス
  
  - ブランチの使い方
  - レビュー指摘後の修正（rebaseやcommit --amendによってコミットをまとめるなど）
- 用語辞書
  
  - 経緯: 最初はGrossaryを用語集として活用していた → Grossaryだけだとカバーできない用語が登場、Grossaryは文章ベースなので使い勝手がイマイチ → 専門のサブWGを用意し、Grossaryを含むこれまでの翻訳結果をもとに用語を抽出して用語集作成 (レビュア中心にたたき台作成してコミュニティで議論)
  - Translator/Reviewerともに用語集にどこまで準拠すればよいかが悩ましい → Level分けをして必須・固有の用語以外はベストエフォートする方向に。
  - 用語集のアップデートや用語をどこまで載せるかが悩ましい → 複合語は基本的に対象外。どのファイルから用語をピックアップしたか(抽出済みファイル一覧)も併せて管理。
- 運営について
  
  - 大手企業様からの参加者が多い中で個人として参加し、みなさんの参加目的と方向性がどこに向いているのかよくわからず、初めの頃はどう話を進めたらいいか戸惑った。（辻田）
- XX

#### 翻訳作業の悩みと対策、日本語固有の悩みと対策

- ドキュメントスタイル崩れ
- 日英表記しないと単語の意味が分からなくなる
- ですます調や句読点の統一も割と日本語固有の話？
- 英文での追記情報箇所（aaa, which xxx など）を日本文にした場合に、同じ文にするのか、文を分けるのか
- 箇条書きを体言止めにするのか否か
- Hyperledger Fabricのコントリビュートルールへの準拠（DCO、リポジトリ最新化方法等）
  
  - 、翻訳WG特有ではないが、初めてのコミュニティ活動参画だったので苦労した
- reStructuredTextやMarkdownの見出しを日本語を使うと、リンクなどが正常に動作しなくなる（非ラテン文字によるもの？）/翻訳前後でURLが変化してしまう（これは言語共通）ので、トピックや節見出しは翻訳しないという妥協案
- 日本語ではスペースを単語区切りとして使わないが、reSTのマークアップでは前後にスペースを必須とするので、誤ってスペースを削除するとマークアップが機能しなくなる、スペースを残すと不自然なスペースが残る（後者にせざるを得ない）
- XX

#### 今後の課題と解決策

- コントリビューター集め
  
  - 貢献バッジを贈呈
  - ミートアップ
  - 翻訳はFabricの勉強になるというメリットを伝える
- 次世代LTSへのキャッチアップ
  
  - Priorityを決めて、優先度高いものからキャッチアップ
  - バッチで差分を取る。
    
    - アップストリームからの同期の仕方、差分の取り方（原文の差分と翻訳文の差分は機械的に照合は困難）、可視化
- コントリビューションの閾値を下げる
  
  - 翻訳に興味を持つ人は、OSS活動は初めてということがある。
  - コントリビューションのプロセスやツールがネックになって、参加が難しいこともある。
  - OSS活動ビギナーが参加しやすい仕組みがあると嬉しい。
- ページビューの集計
  
  - 翻訳ドキュメントをどれぐらいの人が見ているのか気になる。
  - 感想やフィードバックがあれば、聞いてみたい。

#### バックアップ(スライド作成履歴)

#### スライド(ドラフトr1, 2022/07/19)

[![](attachments/thumbnails/22970854/22971600)](attachments/22970854/22971600.pptx)

#### スライド(ドラフトr2, 2022/08/23)

[![](attachments/thumbnails/22970854/22971609)](attachments/22970854/22971609.pptx)

#### スライド(確認用, 2022/09/05)

Ch1-2:

[![](attachments/thumbnails/22970854/22971611)](attachments/22970854/22971611.pptx)

#### ch3-5:

[![](attachments/thumbnails/22970854/22971613)](attachments/22970854/22971613.pptx)

## Attachments:

![](images/icons/bullet_blue.gif) [HyperledgerGlobalForum\_JPDWG\_r1.pptx](attachments/22970854/22971600.pptx) (application/vnd.openxmlformats-officedocument.presentationml.presentation)  
![](images/icons/bullet_blue.gif) [HyperledgerGlobalForum\_JPDWG\_r2.pptx](attachments/22970854/22971609.pptx) (application/vnd.openxmlformats-officedocument.presentationml.presentation)  
![](images/icons/bullet_blue.gif) [BeyondTheLanguageBarrier\_Draft\_Ch1-2.pptx](attachments/22970854/22971611.pptx) (application/vnd.openxmlformats-officedocument.presentationml.presentation)  
![](images/icons/bullet_blue.gif) [HyperledgerGlobalForum\_JPDWG\_r3\_ch3-5.pptx](attachments/22970854/22971613.pptx) (application/vnd.openxmlformats-officedocument.presentationml.presentation)  
![](images/icons/bullet_blue.gif) [BeyondTheLanguageBarrier.pptx](attachments/22970854/22971617.pptx) (application/vnd.openxmlformats-officedocument.presentationml.presentation)

Document generated by Confluence on Nov 26, 2024 16:47

[Atlassian](http://www.atlassian.com/)
