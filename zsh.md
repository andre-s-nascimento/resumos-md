## 📜 Script de Instalação

```bash
#!/bin/bash

# Atualiza pacotes
sudo apt update && sudo apt upgrade -y

# Instala dependências
sudo apt install -y git curl zsh fonts-powerline

# Instala Oh My Zsh
if [ ! -d "$HOME/.oh-my-zsh" ]; then
  sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
fi

# Instala Powerlevel10k
if [ ! -d "${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k" ]; then
  git clone --depth=1 https://github.com/romkatv/powerlevel10k.git \
    ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
fi

# Instala plugins extras
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

git clone https://github.com/zsh-users/zsh-autosuggestions.git \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

git clone https://github.com/zsh-users/zsh-completions.git \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-completions

git clone https://github.com/zsh-users/zsh-history-substring-search.git \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-history-substring-search

# Instala fzf (versão oficial)
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install --all

# Ajusta .zshrc (se não estiver configurado)
if ! grep -q "plugins=(" ~/.zshrc; then
  echo 'plugins=(git zsh-syntax-highlighting zsh-autosuggestions zsh-completions zsh-history-substring-search fzf history copyfile)' >> ~/.zshrc
fi

echo "✅ Instalação concluída. Reinicie o terminal ou rode: source ~/.zshrc"
```

---

## 🚀 O que esse script faz

- Instala **Oh My Zsh**  
- Configura o tema **Powerlevel10k**  
- Adiciona os plugins:  
  - **zsh-syntax-highlighting**  
  - **zsh-autosuggestions**  
  - **zsh-completions**  
  - **zsh-history-substring-search**  
  - **fzf**  
  - history e copyfile (já inclusos no Oh My Zsh)  

---
