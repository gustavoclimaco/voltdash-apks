# voltdash-apks

Arquivos servidos ao VoltDash pela URL raw do GitHub.

O catalogo dos APKs fica em `voltdash-dist/apps.json`; aqui ficam so os arquivos.

## APKs (tela Instalar Apps)

| Arquivo | App | Versao | Pacote |
|---|---|---|---|
| `waze.apk` | Waze | 4.81.0.4 | `com.waze` |
| `revanced-manager.apk` | ReVanced Manager | 3.0.36 | `com.revanced.net.revancedmanager` |

## Arquivos de instalacao (exploit Frida)

Usados pelos scripts de instalacao manual por telnet, para nao depender de
servidor de terceiro. Espelho proprio dos binarios do exploit.

| Arquivo | O que e |
|---|---|
| `fridaserver.rar` | Servidor Frida (binario ELF ARM aarch64, apesar da extensao `.rar`) |
| `fridainject.rar` | Injetor Frida (binario ELF ARM aarch64) |
| `system_server.js` | Hook injetado no `system_server` |

> A extensao `.rar` e mantida so por compatibilidade com os scripts antigos —
> os dois primeiros sao executaveis ELF, nao arquivos RAR.

## Como atualizar

Substitua o arquivo mantendo **o mesmo nome** e faca commit. A URL nao muda,
entao nada quebra no `apps.json` — atualize la apenas o campo `appVersion`,
que e o que decide se o cliente ve o botao "Atualizar".

Repo separado do `voltdash-dist` de proposito: a CI calcula a versao do
VoltDash a partir das tags daquele repo, e releases manuais la sequestrariam
o versionamento.
