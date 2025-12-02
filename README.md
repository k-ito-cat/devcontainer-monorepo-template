# devcontainer-monorepo-template

- devcontainer.base.jsonc - OS 非依存の共通設定
- devcontainer.wsl.jsonc - WSL 専用の設定(1Password SSH agent のマウント)
- devcontainer.json - コピー元に応じて内容が変わるため git 管理対象外とする

使用する OS に応じて`devcontainer.json`を以下のコマンドで作成

## 使い方

### WSL の場合

```bash
cp .devcontainer/devcontainer.wsl.jsonc .devcontainer/devcontainer.json
```

### その他の OS の場合

```bash
cp .devcontainer/devcontainer.base.jsonc .devcontainer/devcontainer.json
```
