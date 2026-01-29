# devcontainer-template

## GUI(VSCode)

`Dev Containers: Reopen in Container`

## CLI

```sh
# 起動
devcontainer up --workspace-folder .

devcontainer exec --workspace-folder . pwd

# シェルに入る
devcontainer exec --workspace-folder . /bin/bash
```

## SSH

// TODO: 対象をagent.sockのみにする

CursorでDevcontainer接続する場合は、CursorはSSH Agentの転送をサポートしていないので以下をdevcontainer.jsonに記述して明示的にマウントすること
```
"mounts": [
  "source=${localEnv:HOME}/.ssh,target=/root/.ssh,type=bind",
  "source=${localEnv:HOME}/.ssh/agent.sock,target=/ssh-agent,type=bind"
],
"remoteEnv": {
  "SSH_AUTH_SOCK": "/ssh-agent"
}
```
