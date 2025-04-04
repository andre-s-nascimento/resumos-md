# ✅ Tutorial: Como Assinar Commits do Git com SSH e Garantir “Verified” no GitHub (Windows 11)

Este guia te ajuda a configurar **commits assinados com SSH no GitHub**, garantindo o selo **"Verified"** nos commits. Vamos usar o Git no Windows 11, com suporte ao PowerShell ou Git Bash.

---

## 🧰 Pré-requisitos

- [x] Git instalado (via [https://git-scm.com](https://git-scm.com))
- [x] Conta no GitHub
- [x] PowerShell ou Git Bash

---

## 1. Gerar uma chave SSH compatível com assinatura

Abra o **PowerShell** ou **Git Bash** e digite:

```bash
ssh-keygen -t ed25519 -C "seu-email@exemplo.com"
```

Aceite o nome sugerido do arquivo (pressione `Enter`) e defina uma **senha forte (opcional, mas recomendada)**.

---

## 2. Copiar a chave pública

```bash
cat ~/.ssh/id_ed25519.pub
```

Copie a saída e vá para:

🔗 [https://github.com/settings/ssh/new](https://github.com/settings/ssh/new)

- Cole a chave
- Dê um nome
- Clique em **Add SSH key**

---

## 3. Obter o caminho da chave SSH para assinatura

Edite sua configuração com o **caminho completo da chave SSH**, não o fingerprint.

### 3.1 Verifique onde está sua chave SSH

O local padrão é:

```powershell
C:\Users\andre\.ssh\id_ed25519
```

### 3.2 Atualize a configuração:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu-email@exemplo.com"
git config --global user.signingkey C:/Users/andre/.ssh/id_ed25519
git config --global gpg.format ssh
git config --global commit.gpgsign true
```

### 3.3 Ou edite o arquivo manualmente:

Abra o `.gitconfig` com:

```powershell
code $HOME\.gitconfig
```

E substitua:

```ini
[user]
    signingkey = SHA256:xxxx...
```

por:

```ini
[user]
    signingkey = C:/Users/andre/.ssh/id_ed25519
```

---

## 4. Iniciar o serviço `ssh-agent` no Windows

⚠️ Execute o PowerShell **como administrador** e digite:

```powershell
Get-Service ssh-agent | Set-Service -StartupType Manual
Start-Service ssh-agent
```

Adicione sua chave ao agente:

```bash
ssh-add ~/.ssh/id_ed25519
```

---

## 5. Testar commit assinado

Crie um repositório ou use um existente:

```bash
git commit -S -m "Remoção de Comentário"
```

Agora, vá até o GitHub e verifique se o commit está com o selo **Verified** ✅.

---

## 🛠 Dica: Verifique as configurações atuais

```bash
git config --list --show-origin
```

---

## 🧯 Erros comuns

Se tiver erro como:

```powershell
error: Couldn't load public key SHA256:xxxxxx: No such file or directory
```

✅ Isso acontece porque você configurou o fingerprint ao invés do **caminho da chave SSH**. Siga os passos da seção 3 para corrigir.

---
