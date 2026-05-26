# Go 環境構築メモ

## 概要
macOS に Homebrew 経由で Go をインストールする手順。

---

## 環境
- OS: macOS（Apple Silicon / Intel）
- パッケージマネージャー: Homebrew

---

## 手順

### 1. Homebrew のインストール
\```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
\```

Apple Silicon の場合は PATH も設定：
\```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
\```

### 2. Go のインストール
\```bash
brew install go
go version
\```

### 3. VSCode の設定
- Go 拡張機能（`golang.go`）をインストール
- `Go: Install/Update Tools` を実行

---

## つまずいたポイント
- Macで初めての環境構築だったためbrewコマンドのインストールから実施した。
---

##go rnの裏側
- go runでバイナリファイルがビルドされ一時ディレクトリに置かれる
- ファイルを実行→終了後バイナリファイル削除

##実行形式ファイル生成
- go build -o hello_world hello.go
-- -o ***にて任意の名前で実行ファイルを生成できる。
## 参考
- [Homebrew 公式](https://brew.sh)
- [Go 公式](https://go.dev)