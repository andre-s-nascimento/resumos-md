# RCLONE

O rclone é uma ferramenta poderosa para gerenciar e transferir arquivos entre seu sistema local e diversos serviços de armazenamento em nuvem. Aqui estão alguns dos comandos básicos do rclone que você pode usar:

## 1. Configuração

Criar uma nova configuração:

```bash
rclone config
```

Este comando inicia um assistente interativo para configurar um novo remote (armazenamento em nuvem).
## 2. Listar remotes

Listar todos os remotes configurados:
```bash
rclone listremotes
```

## 3. Listar arquivos

Listar arquivos em um remote:
```bash
rclone ls remote:path
```

Substitua remote:path pelo nome do seu remote e o caminho desejado.

## 4. Copiar arquivos

Copiar arquivos de um local para um remote:

```bash
rclone copy /caminho/local remote:path
```

Isso copia arquivos do seu sistema local para o remote.

Copiar arquivos de um remote para o local:

```bash
rclone copy remote:path /caminho/local
```

## 5. Sincronizar arquivos

Sincronizar arquivos entre um local e um remote:
```bash
rclone sync /caminho/local remote:path
```

Isso faz com que o local e o remote sejam idênticos, excluindo arquivos no destino que não estão na fonte.

## 6. Mover arquivos

Mover arquivos de um local para um remote:

```bash
rclone move /caminho/local remote:path
```

Mover arquivos de um remote para o local:

```bash
rclone move remote:path /caminho/local
```

## 7. Excluir arquivos

Excluir arquivos em um remote:

```bash
rclone delete remote:path
```

Excluir arquivos em um local:

```bash
rclone delete /caminho/local
```

## 8. Verificar arquivos

Verificar se os arquivos em um remote estão corretos em relação a um local:

```bash
rclone check /caminho/local remote:path
```

## 9. Obter informações

Mostrar informações sobre um remote:

```bash
rclone about remote:path
```

## 10. Ajuda

Obter ajuda sobre qualquer comando:

```bash
rclone help
```

Obter ajuda sobre um comando específico:

```bash
rclone [comando] --help
```

Exemplo de Uso:

Se você configurou um remote chamado onedrive, você pode copiar um arquivo chamado documento.txt do seu diretório atual para uma pasta chamada Documentos no OneDrive com o seguinte comando:

```bash
rclone copy documento.txt onedrive:Documentos/
```

Esses são alguns dos comandos básicos do rclone. Para mais detalhes e opções avançadas, consulte a [documentação oficial do rclone](https://rclone.org/docs/).
