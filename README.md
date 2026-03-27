# zed-setting

[Zed](https://zed.dev/) エディタの設定ファイルを管理するリポジトリ。

## 使い方

シンボリックリンクを作成して Zed の設定ディレクトリに配置する。

### Windows

```powershell
# PowerShell（管理者権限で実行）
New-Item -ItemType SymbolicLink -Path "$env:APPDATA\Zed\settings.json" -Target "<このリポジトリのパス>\settings.json"
```

### macOS

```bash
ln -s <このリポジトリのパス>/settings.json ~/.config/zed/settings.json
```

既に `settings.json` が存在する場合は、先に削除またはバックアップしてからリンクを作成する。
