# HonKit

> HonKit は GitBook から Fork して作られたMarkdownからドキュメントページや書籍を作成するツールです<br/>[Web Scratch](https://efcl.info/2020/06/19/githon/)

<p class="author-comment">HonKitはMarkdownから、HTMLやPDFやePubなどを生成するツール。CMSの一種といえばそうだけど「出版」に特化しており、今どきのCMSに期待される諸所の機能、例えば、FeedやSitemapやOGP...などのネットで参照されるための仕掛け（SEO?）はデフォルトでは組み込まれていない。モチベーションの項でも言及しているが、開発ドキュメントのビューに利用できるが、その運用フローについてHonGitがナニかを担えるわけでもなく、そういう視点ではGitBookの方が目的に叶うかもしれない。フロントエンジニアとしてはNode.jsで動くCMS（Apache Licence）として興味深い。
Autherは [jser.info](http://jser.info/)のazaさん</p>

## 参照
- [honkit/honkit](https://github.com/honkit/honkit)
- [HonKit Toolchain Documentation
](https://honkit.netlify.app/)
- [Web Scratch](https://efcl.info/2020/06/19/githon/)

## モチベーション
システム開発には、設計書とコードの整合性を保つという苦難があります。

ウォーターフォールであれアジャイルであれ、ある一定数以上の開発者とシステム規模になると、どうしてもコードから全てを読むことは難しくなり、コード以外に全体観を把握できるドキュメントが必要になります。（ドキュメント腐る問題）

### GitHubで運用するドキュメントの利便性を向上したい
GitHubでドキュメントを管理するのは、なかなか利にかなったアイデアです。そもそもGitHubは変更履歴を記録・追跡するツールですから変更管理に長けていますし、PRやレビューというフローも適用できます。
エンジニアからすると普段から慣れ親しんでいるツールです。Markdownで書きさえすれば体裁は整えられるのです。

しかしながら、エンジニアではないメンバー（例えば、プランナー/UX/UI）にとっては「見やすい」とも言えません。
具体的には「探しているドキュメントを見つけづらい」等が端的な例です。

## HonKitは何を解決する？
HonKitはGitBookのForkで、GitBookとの多くの共通点があります。（OSSとしてのGitBookとサービスとしてのGitBookがあります）

GitBookの生い立ちまでは追っかけませんが、GitHubで管理するMarkdownを強く意識しているし、その構造化されたビューの生成に長けています。しかし、GitBookはDeprecatedとなって開発は止まっており、代わりに、[GitBook.com](https://www.gitbook.com/)上でのホスティングサービスとなっています。

### GitBook (GitBook.com)も検討すべし
GitBookは、ドキュメント管理で発生するフローに必要な機能（コメントだとか）を備えており、なかなかパワフルです。

### 利点
#### 非エンジニア向けビュワーとして
比較してHonKitがドキュメント管理フローに使えるかと言えば、ちょっと足らないです。しかし、ドキュメントの整理やビュワーとしては、GitHub上のMarkdownを漁るよりは効率が良さそうです。

HonKitのカスタマイズは自由です。プラグインなども開発可能ですからフロントエンジニアとして、面白そうというモチベーションはあります。