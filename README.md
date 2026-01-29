# devcontainer-template

## GUI(VSCode)


## CLI


## SSH

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
