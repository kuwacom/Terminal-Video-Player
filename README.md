# What Is This
このプログラムは、terminal及びconsoleでANSI文字コードを使い、フルカラーもしくはモノクロで動画を再生する物です。

# How To Use
各自環境に合わせて設定してください

例えばpythonコマンドなど...

| OS | コマンド | 例 |
|----|----------|----|
| Windows(PythonLauncher) | `py -<version>` or `py` | `py -3.10 ./main.py` |
| Windows(UWP) | `python` | `python ./main.py` |
| Linux | `python3` | `python3 ./main.py` |

### 注意
**前提条件として、利用するターミナル及びコンソールがANSIエスケープシーケンスに対応している必要があります！**<br>
**`console.color-checker.py`を利用して簡単にテストできますので、利用前にあらかじめ確認してください**

## モジュールのインストール
まずは必要なモジュールをインストールします

```bash
pip install -r req.txt
```

## 実行
後は [#コマンド Docs](#コマンド-docs) を参考にコマンドを実行してください

# コマンド Docs
## 実行ファイル
コンパイルはしていないので、以下のファイルをPythonで実行してください
```
console-video-player.py
```

## 引数
| 引数 | 型 | 説明 | オプション |
|------|----|------|------------|
| - | `str` | 再生するビデオファイルのpath<br>一番最初に書く | 必須 |
| `--loop` | - | ループ再生の有効化 | オプション |
| `--width` | `int` | 幅(どちらか片方を入力すると自動で比率を保つ) | オプション |
| `--height` | `int` | 高さ | オプション |
| `--playAudio` | - | オーディオを再生を無効化 | オプション |
| `--colorMode` | `str` | フルカラーかモノクロか | オプション<br>選択肢: `mono`, `color`<br>デフォルト: `mono` |
| `--fontColor` | `str` | モノクロ時の文字色 | オプション<br>例: `"256,256,256"` |
| `--renderMode` | `str` | consoleへのテキストの描画方法 | オプション<br>選択肢: `once`, `line`<br>デフォルト: `line` |
| `--debug` | - | デバッグモードの有効化<br>フレームレート等を表示する | オプション |

## コマンド例
```bash
python3 ./console-video-player.py ./ui-30.webm --colorMode color --loop --debug
```
上記のコマンドの場合、デバッグ表記を有効化して`ui-30.webm`をカラーモードでターミナルサイズに追従してループ再生する