# devcontainer-template

- devcontainer.base.jsonc - OS 非依存の共通設定
- devcontainer.wsl.jsonc - WSL 専用の設定(1Password SSH agent のマウント)

使用する OS に応じて`devcontainer.json`を以下のコマンドで作成

## 使い方

### WSL の場合

```bash
cp .devcontainer/devcontainer.wsl.json .devcontainer/devcontainer.json
```

### その他の OS の場合

```bash
cp .devcontainer/devcontainer.base.json .devcontainer/devcontainer.json
```
