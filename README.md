# OCCP_SUBOS
OCCP is an on-chain context protocol that treats value transfer and information persistence as equivalent. SUBOS is an experimental terminal built to interact with it.
For details, please refer to the White Paper.

# SUB OS
1,000 bytes.
The practical safety zone is approximately 850 bytes.

In a vessel smaller than even those of the 1990s,
we begin the Internet once more.

But make no mistake—this is not a limitation.

Each record may be small,
yet contexts entwine, persist, and accumulate,
eventually becoming a chronicle without end.

Finite, yet boundless.
A universe infinitely close to infinity.

This is not a service.
It is an experiment in how we walk.

The name is yours. The purpose is yours.
But the record remains.

A voyage beginning from 850 bytes.

Hello World.


<img src="https://github.com/user-attachments/assets/b1f3296b-d905-41bf-80c2-bb801e1cb651" width="300" />


## What is this?
SUBOS is an experimental terminal environment implementing
OCCP (On-Chain Context Protocol).

OCCP explores a simple idea:

Value transfer and information persistence can be treated as the same process on a distributed ledger.

The current reference implementation operates on the XRP Ledger (XRPL),



## ⚠️ Security Warning

SUBOS is experimental software intended for research and exploration.

This application operates inside a web browser environment and interacts
with blockchain accounts and private keys.

Browser environments cannot be considered secure execution spaces.
Malicious scripts, browser extensions, modified source files,
or compromised environments may expose sensitive information.

Security has not been audited.

**Use burner wallets only.**
Never use wallets containing meaningful funds.

If you are not comfortable managing cryptographic keys
and understanding associated risks, do not proceed.

You are solely responsible for your environment, keys, and actions.
using transaction metadata and NFTs as linked contextual storage.

SUBOS is not a platform or service.
It is a tool for writing and linking context directly on-chain.


## 🚀 Quick Start

The English description will be ready soon. Please hold on.

SUB OSの使い方


さて、SUB OSの基本的な機能とその処理を軽く説明します。

まずは【01】の欄にウォレットSEEDを入力します
（安全性を考慮して実験用のウォレットを使ってください）

すると【02】の欄　ストレージ、ストリームディレクトリに作ったストレージが表示されます。
これは技術的には先ほどお話した、NFTを利用してます。

あなたがまだ何も作っていなければ、何も表示されません。

では実際に作っていきましょう。

【03】 BOOT CONTEXT

Stream Label
今回は「DIARY（日記）」をつくりましょう。
DIARYと入れてみてください。

Category (Sort ID) Profile (01) Diary (10) User (20) User (30) User (50) System (80) Default (99)
後に【02】のストレージストリームディレクトリに表示する順番を指定します。
何番でも良いですが、日記は10番を用意してます。


Data Format (Type) 01: Text 02: Web
01のtextで構いません。02は未実装で予約領域です。

Language (Lang) E (English) J (Japanese)
英語なら素直にEnglishで　日本語ならJapaneseです。あまり意味はないかもしれません。

Order 01: Newest 02: Oldest
【05】ストリームヒストリーに表示される順番を降順　昇順に変えます。新しい順か古い順かです。
日記なら最近は01のNewestが良いでしょう。ツイッターの様に「上」に最新の投稿が出てきます。

GENESIS (New Stream)　CHAIN (Append Stream)
新規作成なのか、以前作ったストリーム履歴に連鎖させるか決めます。
初めてならジェネシスでいいです。

Parent Hash / Pointer
チェインの時　もしくはジェネシスの時でも、以前仮想通貨にメモした送金履歴のハッシュを入れれば、そのハッシュを記録してくれます。
チェインの場合新しいメモに古いハッシュを自動的に付与してくれます。
このことにより、文脈が繋がります。（良い説明を考えます）

実際は自動的に入力してくれるよう設計してるのでご安心ください。手作業でも出来るというだけです。


[04] BROADCAST & MINT (The Shouting)

Target (Destination Address)　Test Target
ターゲットを決めます。
実は誰に送金しても自分のNFTが記録するのであまり気にしなくていいのですが、一応指定できます。
テストターゲットとして私の用意したIDに送り付けることが出来ます。

Memo Data (Context Message)
メモする内容です。
「「今日は暑いな　セミが鳴いてる」」
とかでいいです。文字が入るという事はデータも工夫すれば入れれるでしょう。


さぁ、EXECUTE SEQUENCEを押しましょう。
コンソールログがかっこよく走ります。OSは落とさないでください。

送金（メモ）をノードに送り、ノードが受け取った印（ハッシュ）を此方に送り返します。
そのハッシュをNFTにメモしNFTを発行します。（だからこの作業が終わるまで落としたらダメなのです。）

完了すると【02】ストレージ　ストリームディレクトリに
DIARY　という物（NFT）が追加され
最後はそのNFTに紐づいた送金のメモを【05】ストリームヒストリーに表記します。


チェーンの場合
【02】ストレージストリームディレクトリに先ほど作ったDIARYがあります。
それを選択すると【03】 BOOT CONTEXTのほとんどの欄とハッシュが自動入力されます。

最終投稿が「「今日は暑いな、セミが鳴いてる」」だと、そのハッシュが入力されています。
後は【04】の欄を先ほどと同じように入力して、日記の続きでも書けばいいでしょう。

EXECUTE SEQUENCEで先ほどの様に処理が走ります。
