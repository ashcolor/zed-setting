# zed-setting

[Zed](https://zed.dev/) エディタの設定ファイルを管理するリポジトリ。

## ファイル構成

- `settings-macos.json` — macOS 用設定
- `settings-windows.json` — Windows 用設定（Git Bash をターミナルシェルに指定）

## 使い方

シンボリックリンクを作成して Zed の設定ディレクトリに配置する。

### macOS

```bash
ln -s <このリポジトリのパス>/settings-macos.json ~/.config/zed/settings.json
```

### Windows

```powershell
# PowerShell（管理者権限で実行）
New-Item -ItemType SymbolicLink -Path "$env:APPDATA\Zed\settings.json" -Target "<このリポジトリのパス>\settings-windows.json"
```

既に `settings.json` が存在する場合は、先に削除またはバックアップしてからリンクを作成する。
