# M5Core2_Avatar_VoiceText_TTS_Blynk
M5Core2_Avatar_VoiceText_TTS_Blynk

---
### [注意]M5Unified版を作ったのでこちらを使うことをお勧めします。 ###

* [M5Unified_Avatar_VoiceText_TTS_Blynk](https://github.com/robo8080/M5Unified_Avatar_VoiceText_TTS_Blynk/ "Title")<br>

---


M5Stack Core2で、M5Stack-AvatarとHOYA社が提供する[VoiceText Web APIサービス](https://cloud.voicetext.jp/webapi "Title")を使った音声合成(TTS)を動かすテストプログラムです。


VoiceText TTSは、kghrlaboさんのesp32_text_to_speechを参考にさせていただきました。<br>
オリジナルはこちら。<br>
esp32_text_to_speech <https://github.com/kghrlabo/esp32_text_to_speech><br>

---

### 必要な物 ###
* [M5Stack Core2 または M5Stack Fire](http://www.m5stack.com/ "Title") (M5Stack Core2、M5Stack Core2 for AWS、M5Stack Fireで動作確認をしました。)<br>
* Arduino IDE (バージョン 1.8.15で動作確認をしました。)<br>
* [M5Stack-Avatar](https://github.com/meganetaaan/m5stack-avatar/ "Title")ライブラリ(バージョン 0.7.4で動作確認をしました。)<br>
* [ESP8266Audio](https://github.com/earlephilhower/ESP8266Audio/ "Title")ライブラリ(バージョン 1.9.3で動作確認をしました。)<br>
* [Blynk](https://blynk.io/ "Title")ライブラリ(バージョン 1.0.1で動作確認をしました。)<br>
* ボードマネージャー arduino-esp32 (v1.0.6で動作確認をしました。) <br>
* M5Stack Core2を使用するときはM5Core2ライブラリ 0.1.3 (0.1.4以降だと音がおかしくなるようです。)<br><br>


### WiFiの設定 ###
* M5Core2_Avatar_VoiceText_TTS_Blynk.inoの15行目付近、SSIDとPASSWORDを設定してください。

### Blynk Auth Tokenの設定 ###
* M5Core2_Avatar_VoiceText_TTS_Blynk.inoの21行目付近、YOUR_BLYNK_AUTH_TOKENを設定してください。<br>
Blynk Auth Tokenは、[ここ](https://docs.blynk.cc/ "Title")から取得してください。。<br>


### VoiceText Wev API api キーの設定 ###
* AudioFileSourceVoiceTextStream.cppの30行目付近、YOUR_TSS_API_KEYを設定してください。<br>
APIキーは、[ここ](https://cloud.voicetext.jp/webapi/ "Title")の「無料利用登録」から申請すれば、メールで送られて来ます。<br>

### 使い方１ ###
1. 'ping blynk-cloud.com'で、BlynkのサーバーのIPアドレスを調べてください。 <br>
2. ブラウザから下記のようにアクセスしてください。 V1、V2、V3、それぞれ異なった声でしゃべります。<br>
http://188.166.206.43/YOUR_BLYNK_AUTH_TOKEN/update/v1?value=こんにちは世界！<br>
http://188.166.206.43/YOUR_BLYNK_AUTH_TOKEN/update/v2?value=こんにちは世界！<br>
http://188.166.206.43/YOUR_BLYNK_AUTH_TOKEN/update/v3?value=こんにちは世界！<br><br>

### 使い方２ ###
* M5Stack Core2のボタンA,B,Cを押すと、それぞれ異なった声でしゃべります。　<br><br>

TTSのパラメータの詳細はこちらを参照してください。<br>
[VoiceText Web API [API マニュアル](https://cloud.voicetext.jp/webapi/docs/api/ "Title")]
<br><br><br>

