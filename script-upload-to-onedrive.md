# upload-to-one-drive

Para criar um script em Bash que envia um arquivo local para o OneDrive a cada hora, você pode usar o rclone em conjunto com um cron job.

## Passo 1: Criar o Script Bash

Crie um arquivo de script. Vamos chamá-lo de upload_to_onedrive.sh:

```bash
nano ~/upload_to_onedrive.sh
```

Adicione o seguinte conteúdo ao script:

```bash
#!/bin/bash

# Caminho do arquivo local que você deseja enviar
LOCAL_FILE="/caminho/para/seu/arquivo.txt"

# Destino no OneDrive
ONEDRIVE_DEST="onedrive:/pasta/destino/"

# Comando para copiar o arquivo
rclone copy "$LOCAL_FILE" "$ONEDRIVE_DEST"
```

Substitua /caminho/para/seu/arquivo.txt pelo caminho do arquivo que você deseja enviar.

Substitua onedrive:/pasta/destino/ pela pasta de destino no OneDrive.

Salve e feche o arquivo. Se você estiver usando o nano, pressione CTRL + X, depois Y, e em seguida Enter.

Torne o script executável:

```bash
chmod +x ~/upload_to_onedrive.sh
```

## Passo 2: Configurar o Cron Job

Abra o crontab para edição:

```bash
crontab -e
```

Adicione a seguinte linha ao final do arquivo para executar o script a cada hora:

```bash
0 * * * * /bin/bash ~/upload_to_onedrive.sh
```

Isso fará com que o script seja executado no início de cada hora (por exemplo, 1:00, 2:00, 3:00, etc.).

Salve e feche o crontab. Se você estiver usando o nano, pressione CTRL + X, depois Y, e em seguida Enter.

## Considerações Finais

Verifique se o rclone está corretamente configurado e acessível a partir do terminal. Você pode testar o comando manualmente antes de deixar o cron job rodar.

Se você quiser verificar os logs do cron, você pode redirecionar a saída do script para um arquivo de log. Para isso, você pode modificar a linha do crontab assim:

```bash
0 * * * * /bin/bash ~/upload_to_onedrive.sh >> ~/upload_log.txt 2>&1
```

Isso irá registrar a saída e os erros do script no arquivo upload_log.txt.

Agora, seu script deve rodar automaticamente a cada hora, enviando o arquivo especificado para o OneDrive!
