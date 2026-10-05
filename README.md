# Voice Valet

各音声合成ソフトの「音声再生」「音声保存」を代わりにやってくれたりと、音声合成ソフトを使った動画編集する方のサポートを提供するAviUtl2 用のプラグインです。

同様のショートカットを提供することと、プロジェクトで利用する音声合成ソフトをプリセットとして保存しておくことで、プロジェクトファイルを開いた際に自動で開いてくれる機能を提供します。

## 動作環境

- AviUtl2 2.1.11 以上
- Windows 10 / 11（64bit）

## インストール

### Aviutl2カタログの場合

Aviutl2カタログで「Voice Valet」と検索して頂き、インストールボタンを押せば完了となります。

### 自分で導入する場合

次のステップでインストールすることが可能です。

1. [Releases](https://github.com/Tksn07/aviutl2-voice-valet/releases) から最新の `voice_valet.aux2` をダウンロード
2. AviUtl2 の Plugin フォルダ（例: `C:\ProgramData\aviutl2\Plugin`）に入れる
3. AviUtl2 を起動し直す

## 主な機能

Voice Valetでは次の機能を提供しています。

1. 🎙 ボタン1つで音声保存
2. ⌨️ ショートカットキーで保存・再生
3. 📁 ファイル名と保存先をきれいに整理
4. 🗂 プリセット（作品ごとの作業環境をまとめて切り替え）
5. 🔗 Voice Drop のルールを自動で作成

## 動画でもご紹介

[ニコニコ動画のリンク]


## Voice Valet の使い方


Voice Valetを導入して頂けた方の為に、Voice Valetの基本的な使い方の説明を行います。

導入が完了しましたら、まず最初にAviutl2の左上にある「表示」から「Voice Valet」を選択してください。すると、最初にこのような画面が表示されます。

<img width="785" height="528" alt="image" src="https://github.com/user-attachments/assets/2ad983e9-dafb-42b1-b7b1-425f61168d48" />

このままだと使いにくいと思うので、プラグインを右クリックし、「ウィンドウ配置」→「ウィンドウ分離」を選択しておくと見やすい形で表示してくれます。

<img width="577" height="464" alt="image" src="https://github.com/user-attachments/assets/3090410a-0e14-4e10-b9fe-2d3fb535a58b" />

### ファイル選択

---

まず最初にファイル選択をします。ここで選択するファイルはこのプラグイン経由で保存した音声やテキストをどのファイル配下に置くかを決めます。

例えば、`E:\Aviutl2\voice-valet` を選択すると、そのファイル配下に音声とテキストが溜まっていきます。

<img width="623" height="462" alt="スクリーンショット 2026-10-05 230052" src="https://github.com/user-attachments/assets/5d2f9e3b-af38-44b6-a25e-c78d363849c7" />

### 音声合成ソフトを開き、プラグイン経由で音声保存をしてみる

voicevoxを例で利用してみます。

voicevoxを開いて適当にテキストを入力します。

<img width="1184" height="677" alt="image" src="https://github.com/user-attachments/assets/39ee8427-2d08-4959-acd5-f8f88224886c" />

その状態で、 `Ctrl+Shift+Space` を押してみてください。すると音声が再生されます。

次に、 `Ctrl+Shift+R` を押してみてください。すると `yyyyMMddhhmmss_キャラクター名_テキスト` というファイル名で音声が保存されます。

このようにショートカットを提供するのがこのプラグインの1つ目の機能になります。

voicevoxを例にしましたが、このプラグインでは次のソフトに対応しています。

同じショートカットキーで複数の音声合成ソフトの音声再生・音声保存を可能にするため、ソフトごとにショートカットキーを覚えるなどの面倒事を無くすことを目的に作成しています。

### Voice Valetの使い方（２）

---

もう一つのメイン機能の紹介です。

Voice Valetではプロジェクト毎にそのプロジェクトで利用する音声合成ソフトを「プリセット」として保存し、プロジェクトを立ち上げた際、自動で音声合成ソフトと各ソフトのプロジェクトファイルを開く事が可能です。

例でこちらの編集中のプロジェクトがあったとします。

<img width="1870" height="1000" alt="image" src="https://github.com/user-attachments/assets/4d1919ee-a9f6-4176-8fc1-0397965aeef0" />

1. Aviutl2で、`test.aux2` というプロジェクトの編集中です
2. このプロジェクトでは「Voicevox」「AIVoice2」を利用しています
3. Voicevoxは `voice_valet_voicevox.vvproj` というプロジェクトファイルを開いてます
4. AIVoice2は、`voice_valet_AIVoice.aieprojx` というプロジェクトファイルを開いています

#### この状態を次開いた時にも同じようにするために「プリセット」として保存する

---

この状態で編集を行って、明日また同じように編集を進めたい時があるかもしれません。その時、Aviutl2のプロジェクトを開いて、各音声合成ソフトを立ち上げてプロジェクトを開くのは面倒だと思います。

現在のAviutl2のプロジェクトファイルと各ソフトを開いた状態で、右上の「設定」ボタンを押します。

<img width="600" height="432" alt="スクリーンショット 2026-10-05 232219" src="https://github.com/user-attachments/assets/4daf6fc9-3541-4f25-b2d0-a7248baba356" />

「プリセット」を押します。

<img width="604" height="429" alt="image" src="https://github.com/user-attachments/assets/4f179e1e-a0bc-4db8-ab86-a27750acad6d" />

「現在の状態をプリセットとして保存」を押します。

すると現在開いているAviutl2のプロジェクト、各音声合成ソフト、音声合成ソフトで開いているプロジェクトファイル　が取得可能になります。

<img width="606" height="596" alt="image" src="https://github.com/user-attachments/assets/47235e30-f91f-4a61-bc19-5cda08f7bbb3" />

このまま「保存」を押して頂くと現在のプロジェクト状態をプリセットとして保存することが出来ます。

<img width="605" height="592" alt="image" src="https://github.com/user-attachments/assets/09e4606d-2f35-445f-ad1f-31c8034aa739" />

その後、一度各音声合成ソフト、Aviutl2を閉じます。閉じた後、Aviutl2を再び開き、同じプロジェクトファイルを開きます。

<img width="777" height="536" alt="image" src="https://github.com/user-attachments/assets/ec9f8426-6a27-42a8-b9cd-08d2aa9472d5" />

するとこのようなダイアログが表示されます。

<img width="393" height="243" alt="image" src="https://github.com/user-attachments/assets/26bce9f9-8dc5-408b-a961-de76fd0ec0da" />

こちらをOKを押すと、先ほどプリセットとして保存した音声合成ソフトが起動し、Aviutl2のプロジェクトを開くだけで、そのプロジェクトで利用しているソフトとプロジェクトを自動で開いてくれる機能になります。

<img width="1872" height="1002" alt="image" src="https://github.com/user-attachments/assets/64817303-6a20-4eec-9c92-be0fc4a42d38" />

主に、数日かけて編集する方が最初の起動の楽をするための機能です。

## その他細かい機能

Voice Valetは音声合成ソフトxAviutl2で動画投稿を行っている方に対して、音声合成ソフトによる手間を削減し効率化を目的とした機能を提供しています。

### Voice Dropとの連携

音声合成ソフトから出力された音声とテキストをAviutl2に自動でドロップするプラグイン「Voice Drop」があります。

本プラグインとVoice Dropを利用すると、ショートカットによる音声とテキスト保存～Aviutl2に自動ドロップまでを行うことが出来ます。

Voice Drop側では度のレイヤーにドロップさせるかなどのルールの設定を行う必要があります。

そのルール設定の手間を削減することを目的として、Voice Dropというタブを用意しています。

「設定」→「VoiceDrop」を選択します。

<img width="609" height="598" alt="image" src="https://github.com/user-attachments/assets/b65315f5-4d2a-4566-9940-967a25be7963" />

「起動中のソフトから読み込む」を押します。すると現在立ち上げている音声合成ソフトを選択することが出来ます。

<img width="601" height="345" alt="image" src="https://github.com/user-attachments/assets/12a55d8f-38be-4eb4-b8a4-895cb12fc3ab" />

こちらから「A.I.VOICE2 Editor」を選択してみます。すると選択したソフトから出力されるVoiceDropのルールを生成することが出来ます。

<img width="605" height="607" alt="image" src="https://github.com/user-attachments/assets/12ac7bd2-84d4-49a9-90d2-4bd0f3eca550" />

自分で好きなように編集し、右下の「ルールのエクスポート」を押します。

<img width="599" height="411" alt="image" src="https://github.com/user-attachments/assets/d0dc1334-ac05-4fa4-b565-f6a4d64199e9" />

すると、 `voice-drop-rules.json` が作成されます。

こちらのファイルをVoiceDrop側の「インポート」ボタンを押して、読み込ませます。

<img width="478" height="439" alt="スクリーンショット 2026-10-05 235314" src="https://github.com/user-attachments/assets/223d882d-6438-43d2-a5b8-846d2e7df3f4" />

すると、VoiceDrop側にルールが生成されます。

<img width="553" height="398" alt="スクリーンショット 2026-10-05 235450" src="https://github.com/user-attachments/assets/c62a3573-5993-4c46-975c-78cc4a156f28" />

これでVoiceDrop側のルール設定が完了します。あとは、ショートカットキーを利用したVoice Valet経由で音声を保存した際、Voice Dropがルールに反応し、Aviutl2にドロップされるようになります。

### ショートカットキーを変更したい

このプラグインのショートカットは

- 音声再生：Ctrl+Shift+Space
- 音声保存：Ctrl+Shift+R

になっています。ですが、人によっては別のショートカットキーを割り振りたいと思う人もいると思います。

その方の為に、設定タブに「ホットキー」という欄を用意しています。こちらの設定ボタンを押して頂くと自由に設定することが可能です。

<img width="608" height="410" alt="スクリーンショット 2026-10-05 235714" src="https://github.com/user-attachments/assets/e201b5b7-a23f-4a5b-b360-c965c16ec16f" />

<img width="607" height="412" alt="image" src="https://github.com/user-attachments/assets/8cfcaf8e-66b7-4380-a485-38315cd97e53" />

### 保存ファイル名は各ソフトが決めた保存名にしたい

このプラグインではプラグイン経由で出力される音声とテキストのファイル名は「yyyyMMddhhmmss_キャラクター名_テキスト10文字」で出力されます。

人によっては、ショートカットキーやプリセット機能は使いたいけど、ファイル名はソフト固有のファイル名にしたい。という方もいるかもしれません。

その方のために、「ファイル名形式」という欄を用意しています。

<img width="603" height="450" alt="スクリーンショット 2026-10-06 000314" src="https://github.com/user-attachments/assets/416b1576-7436-452b-a035-a33f3f5d6699" />

こちらの「このファイル名で保存するソフト」の欄にチェックマークを用意しています。こちらのチェックマークをOFFにしてもらうと、ソフト側の音声保存のルールで音声保存がされるようになります。

### キャラクター名でファイルを分けたい

人によっては、キャラクター毎にファイルを管理し保存したい方いると思います。

その方の為に、「保存オプションのキャラクター毎にファイルを分けて保存」を用意しています。

こちらをONにしてもらうと、キャラクター毎にファイルが作成されるようになります。また、もしファイルが分離してしまったり、ファイルで保存されなかった場合、下のテキストにある所にファイル名に必ず含まれているキャラクター名を入れて「追加」を押してもらえると、そのキャラクターでファイルが作成されるようになります。

<img width="600" height="498" alt="image" src="https://github.com/user-attachments/assets/fd474cc4-f1ed-4452-b16a-18debb0e245e" />

### ファイル保存先はVoiceDropと連動させたい。

Voice Drop も導入されている方で、VoiceValetから出力される音声とテキストはVoiceDropが指定しているファイルと常に連動するようにしてほしい。と思う方もいると思います。

その方の為に、「保存先設定」を用意しています。こちらを「Voice Dropの選択中フォルダと連動する」を押して頂くとVoice Drop側で選択されているフォルダを参照し常に連動してくれるようになります。

<img width="602" height="504" alt="スクリーンショット 2026-10-06 001026" src="https://github.com/user-attachments/assets/9d6f9268-6d02-431a-8282-f243d41c3752" />



#### 対応ソフト

| ソフト | 音声保存 | 音声再生 | キャラクター読み込み（VoiceDrop タブ） |
|---|:---:|:---:|:---:|
| VOICEROID2 Editor | ✅ | ✅ | ✅ |
| A.I.VOICE Editor | ✅ | ✅ | − |
| A.I.VOICE2 Editor | ✅ | ✅ | ✅ |
| VOICEPEAK | ✅ | ✅ | ✅ |
| VoiSona Talk Editor | ✅ | ✅ | ✅ |
| CeVIO AI | ✅ | ✅ | ✅ |
| CeVIO CS（Creative Studio） | ✅ | ✅ | ✅ |
| VOICEVOX | ✅ | ✅ | ✅ |
| COEIROINK v2 | ✅ | ✅ | ✅ |

このプラグインでは次の音声合成ソフトに対応しております。また、今後新しい音声合成ソフトが追加され次第対応していく予定です。



## 使う前に確認してほしい、ソフト側の設定

一部のソフトは、次の設定にしておく必要があります。設定が合っていないときは、保存時に Voice Valet が案内を表示します。

| ソフト | 必要な設定 |
|---|---|
| A.I.VOICE Editor | 「ツール > 環境設定」の「音声保存時に毎回設定を表示する」をオン |
| VOICEVOX | 設定の「書き出し先を固定」をオフ |
| COEIROINK v2 | 設定の「書き出し先を固定」をオフ |
| VOICEPEAK | 「環境設定 > キー」で、ブロックの出力と再生にキーが割り当てられていること（初期設定のままなら何もしなくて大丈夫です） |

上の表にないソフトは、特に設定しなくても使えます。

## ご注意

- Voice Valet は、音声合成ソフトの画面を自動で操作して保存します。ソフトのアップデートで画面の作りが変わると、うまく動かなくなることがあります
- 保存が終わるまで（ボタンが「音声保存中」の間）は、音声合成ソフトの画面を触らずにお待ちください
