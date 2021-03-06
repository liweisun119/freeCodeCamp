# freeCodeCamp のリソースを翻訳する方法

あなたの言語に関わらず、学習リソースを提供することが私達の夢です。 この大規模な取り組みを支援するため、私達のオープンソースのコードベースとカリキュラムをローカライズ支援ツール [Crowdin](https://crowdin.com/) と統合しました。

翻訳のワークフローは大きく二つに分かれています。

- カリキュラム、ドキュメント、UI 要素 (ボタン、ラベル等) の**翻訳**

  [私達の翻訳プラットフォーム](https://translate.freecodecamp.org)にサインアップすると、翻訳者として 30 種類以上の言語の翻訳に貢献することができるようになります。

- 上記全ての翻訳の**校正**

  校正者は、コミュニティによって提供された翻訳のトーンが統一されていること、誤字脱字等の一般的な問題がないことを確認します。 要するに、翻訳が高品質であることを保証します。 理由があって私達は機械翻訳を使用していません。

> [!WARNING] 現在、GitHub を使用してファイルを直接翻訳することはなくなりました。以前コントリビューターだった方は、代わりに[翻訳プラットフォーム](https://translate.freecodecamp.org/)を使用してください。

## コントリビューションの心構え

> freeCodeCamp ローカリゼーションロードマップ – スピード制限はありません。

あなたはいつでも、好きなだけ翻訳することができます。 問題となるのは、あなたがボランティアの翻訳者としてどれだけの時間とエネルギーを費やしても構わないと考えているかだけです。

以下のことをご了承ください:

1. **翻訳はチームでの活動です。**

   freeCodeCamp のリソースの翻訳は、コントリビューターとして最も楽しくやりがいのある経験の一つであり、あなたと同じ言語を話す友人や同僚を巻き込むとよりうまくいくでしょう。

   翻訳を始める前に、仲間と共に[コミュニティフォーラム](https://forum.freecodecamp.org/c/contributors/3)や [contributors チャットルーム](https://chat.freecodecamp.org/channel/contributors)に参加して、翻訳に参加したいと伝えることをお勧めします。 翻訳は Crowdin によって貢献しやすくなっていますが、それでも大変な作業です。

   私達はあなたが楽しんで貢献できて、燃え尽きたり興味を失ったりしないよう望んでいます。

   ある言語の翻訳を始めるには 4、5 人の小さなグループで始めるのが良いでしょう。 その後、さらに多くの仲間を募集することもできます。

2. **各言語ごとのサーバーを運用するには多くのコストがかかります。**

   表面的には複雑な技術スタックに見えないかもしれませんが、エンジンを動かし続けるにはかなりのコストがかかります。 これには追加のサーバーを準備することやスタッフをその管理に専念させることも含まれます。

   freeCodeCamp.org はいつも通りこれらを無料で提供することをお約束しますが、最も必要としている人々に優先的にリソースを割り当てる必要があります。 私達が最も避けたいのは、翻訳の活動が停止して内容が古くなってしまい、その言語のサーバーをシャットダウンしなければならなくなることです。

   ある言語でカリキュラムの少なくとも 2、3 の認定講座の翻訳が完了すると、私達はその言語を [`/learn`](https://www.freecodecamp.org/learn) にデプロイする作業を始めることができます。同時に残りの認定講座の翻訳を続けることができます。

   例えば、新しい言語を初めて公開するときには、少なくとも全てのフロントエンドの認定講座を揃えてデプロイしたいと考えています。

3. **翻訳プラットフォームのリストにない言語はどうしたらいいですか？**

   私達はユーザー層を調査し、最も広く使われている言語を 30 以上翻訳プラットフォームに追加しました。 中国語、スペイン語などいくつかの言語はすでに **"/learn"** にデプロイされています。

   残念ながら、リストにない言語も多数あります。 コントリビューターの皆さんから、彼らの言語への翻訳を手伝いたいというリクエストが毎日たくさんあります。

   もちろん更に多くの言語をリストに追加したいと思っていますが、ご想像の通り、その言語に十分な勢いがなければ実現できません。

   新しい言語を追加したい場合、あなたの友人を誘って興味を持ってもらうことをお勧めします。

   興味を持ってコミットできる少人数 (最低 4、5 人) のグループが集まったら、電話会議でお話させていただきます。 そこで詳細と、いくつかのツールやプロセスについてご説明します。

## 翻訳を始めるには

まず、[contributors チャットルーム](https://chat.freecodecamp.org/channel/contributors)で挨拶をしましょう。 私達はここでリソースの翻訳に関する最新情報を投稿したり、多くの質問に答えたりしています。

次に、私達の[翻訳プラットフォーム](https://translate.freecodecamp.org/)にアクセスし、ログインしてください (初めての場合、アカウントを作成する必要があります)。

最後に、翻訳ツールとワークフローについて理解するため、以下の詳しい説明をお読みください。

それでは翻訳をお楽しみください！

## プロジェクトとファイルを選択する

翻訳プラットフォームにアクセスすると、翻訳可能な「プロジェクト」が複数表示されます。

1. [Contributing documentation](https://translate.freecodecamp.org/contributing-docs) プロジェクトには、このドキュメンテーションサイトのファイルが入っています。
2. [Coding Curriculum](https://translate.freecodecamp.org/curriculum) プロジェクトには、カリキュラムのチャレンジのファイルが入っています。
3. [Learn User Interface](https://translate.freecodecamp.org/learn-ui) プロジェクトには、学習プラットフォームのボタン、ラベル等の UI 要素の文言が入っています。

貢献したいプロジェクトを選択してください。翻訳可能な言語の一覧が表示されます。

![画像 - 選択可能な言語のリスト](https://contribute.freecodecamp.org/images/crowdin/languages.png)

作業したい言語を選択すると、ファイル一覧がツリー状に表示されます。

![画像 - 選択可能なファイルのリスト](https://contribute.freecodecamp.org/images/crowdin/file-tree.png)

それぞれのファイル、フォルダに対しプログレスバーが表示されます。 プログレスバーの**青色**はファイルがどれだけ翻訳されたかを示しています。**緑色**は校正チームによってどれだけ承認されたかを示しています。

作業するファイルを選択すると、Crowdin のエディター画面が表示されます。

> [!NOTE] エディター画面を開いた後、設定アイコン (歯車のアイコン) をクリックし、「HTML tags displaying」の設定を「SHOW」に変更する必要があります。 これで、`<0></0>` ではなく `<code></code>` などのタグが表示されるようになります。

## カリキュラムを翻訳する

![画像 - 編集画面](https://contribute.freecodecamp.org/images/crowdin/editor.png)

Crowdin はドキュメントを翻訳可能な文字列 (通常は文単位) に分割しています。 それぞれの文字列を個別に翻訳します。 上記の画像を参照してください。

1. 緑でハイライトされた文字列は、既に翻訳案が提出されています。
2. 赤でハイライトされた文字列は、まだ翻訳案が_ありません_。
3. グレーアウトされている文字列は翻訳することができません。 これはコードブロックなど、翻訳すべきではない内容が該当します。 この文字列はエディター上で選択できません。
4. 既にコントリビューターが翻訳を提案している場合、Crowdin はその翻訳案をこちらに表示します。 あなたは全く同じ翻訳案を保存することはできません。代わりに、翻訳内容が正確であれば `+` アイコンをクリックし、賛成票を投じてください。 不正確な翻訳の場合、`-` アイコンで反対票を投じることができます。
5. Crowdin は Translation Memory (TM) もしくは Machine Translation (MT) に基づいて翻訳案を推薦します。 Translation Memory とは、他のファイルにおいて翻訳・承認された、類似または同一の文字列を指します。 Machine Translation とは、Crowdin の統合ライブラリーによって推薦された翻訳を指します。
6. こちらがエディター領域です。選択した文字列に対する翻訳案を記述することができます。
7. 現在エディター上で選択されている文字列は黄色でハイライトされます。
8. こちらには文字列の状態を表すタグが表示されます。 `Done` は、文字列に対し少なくとも 1 つ翻訳案があることを意味します。 `Todo` は、文字列に対しまだ翻訳案がないことを意味します。
9. こちらはコメントウィンドウです。 もし特定の文字列に対し疑問や懸念があれば、ここにコメントを残して他の翻訳者に見てもらうことができます。
10. この 2 つのボタンで左側 (ドキュメント部分) と右側 (コメント部分) を隠すことができます。

> [!NOTE] もし翻訳が含まれている隠し文字列を見つけたら [contributors チャットルーム](https://chat.freecodecamp.org/channel/contributors)にてお知らせください。該当箇所をメモリーから削除します。

文字列の翻訳が終わったら、`Save` ボタンを押して翻訳を Crowdin に保存してください。 これで他のコントリビューターが翻訳内容に対し投票したり、校正者が承認したりできるようになります。

翻訳を行う文字列の数に制限はありません。1 つのファイルをすべて翻訳し終わったあとや、新しい翻訳を提案する際に追加で必要になる手順もありません。 `Save` ボタンをクリックするだけで、翻訳を保存できます。

> [!NOTE] もし英語の原文ファイルの中に不正確な内容を見つけた場合、翻訳作業の一環では修正しないでください。 代わりに、相違点があることをその文字列に対するコメントでお知らせいただくか、GitHub issue を作成してください。

## ドキュメントを翻訳する

コントリビューションドキュメントの翻訳も、カリキュラムのファイルの翻訳と同じような流れです。

> [!NOTE] コントリビューションドキュメントは `docsify` によって提供されており、このようなメッセージボックス用に特別な構文解析機能があります。 `[!NOTE]`、`[!WARNING]` または `[!TIP]` などで始まる文字列を見かけたら、これらの単語は翻訳しないようにしてください。

## 翻訳を評価する

Crowdin では既に提出されている翻訳案を評価することができます。 翻訳内容を保存しようとした際、同じ翻訳は保存できないというメッセージが表示されることがあるかもしれません。これは、他のコントリビューターがすでに全く同じ翻訳を提案していることを意味しています。 その翻訳内容に賛成であれば `+` ボタンをクリックして賛成票を投じてください。

もし、不正確または元の文字列と同程度に明確でない翻訳案を見かけた場合、`-` ボタンをクリックして反対票を投じてください。

Crowdin はこれらの投票を元にそれぞれの翻訳案の点数を算出します。これは校正チームがどの翻訳案が最適かを決定するのに役立ちます。

## 品質保証チェック

翻訳内容が可能な限り正確であることを確認するために、幾つかの品質保証のステップを設けています。これにより校正チームが翻訳案をレビューしやすくなります。

翻訳内容を保存しようとした際、内容に対する警告文が表示されることがあります。

![画像 - 品質保証用警告メッセージ](https://contribute.freecodecamp.org/images/crowdin/qa-message.png)

このメッセージは、Crowdin の品質保証システムが翻訳案に潜在的なエラーを検出したときに表示されます。 上の例では、`<code>` タグ内のテキストが変更されており、Crowdin がそれを検出しました。

> [!WARNING] エラーが検出されても翻訳内容を保存することは可能です。 「Save Anyway」をクリックして保存できますが、その場合は校正者かプロジェクトマネージャー宛てにタグ付けし、なぜ品質保証メッセージを無視する必要があったかを説明するようにしてください。

## 翻訳のベストプラクティス

翻訳内容を可能な限り正確なものとするため、以下のガイドラインに従ってください。

- `<code>` タグの中身は翻訳しないでください。 これらのタグはコード内のテキストを意味しており、英語のまま残しておかなければなりません。
- コンテンツを追加しないでください。 もしコーディングチャレンジに対し、テキスト内容の変更や追加の情報が必要だと感じた場合、GitHub issue、または該当の英語ファイルを変更する pull request を通して変更を提案してください。
- コンテンツの順番を変えないでください。

質問があれば、[contributors チャットルーム](https://chat.freecodecamp.org/channel/contributors)にてお気軽にお尋ねください。喜んでサポートいたします。
