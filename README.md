# voltdash-apks

APKs de terceiros oferecidos na tela **Instalar Apps** do VoltDash.

O catalogo em si fica em `voltdash-dist/apps.json`; aqui ficam so os arquivos.

| Arquivo | App | Versao | Pacote |
|---|---|---|---|
| `waze.apk` | Waze | 4.81.0.4 | `com.waze` |
| `revanced-manager.apk` | ReVanced Manager | 3.0.36 | `com.revanced.net.revancedmanager` |

## Como atualizar

Substitua o arquivo mantendo **o mesmo nome** e faca commit. A URL nao muda,
entao nada quebra no `apps.json` — atualize la apenas o campo `appVersion`,
que e o que decide se o cliente ve o botao "Atualizar".

Repo separado do `voltdash-dist` de proposito: a CI calcula a versao do
VoltDash a partir das tags daquele repo, e releases manuais la sequestrariam
o versionamento.
