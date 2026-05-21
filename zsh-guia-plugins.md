# Guia de Plugins Zsh

Este documento explica os plugins configurados no `.zshrc`, como instalar e como usar cada um.

---

## git
**Descrição:** Adiciona dezenas de aliases e funções para facilitar o uso do Git.  
**Instalação:** Já incluso no Oh My Zsh. Basta manter `git` na lista de plugins.  
**Uso:**  
- `gst` → `git status`  
- `gco` → `git checkout`  
- `gcmsg "msg"` → `git commit -m "msg"`

---

## zsh-syntax-highlighting
**Descrição:** Destaca comandos digitados no terminal (verde para válidos, vermelho para erros).  
**Instalação:**  
```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
**Uso:** Digite qualquer comando e veja a cor mudar conforme a validade.

---

## zsh-autosuggestions
**Descrição:** Sugere automaticamente comandos já usados no histórico.  
**Instalação:**  
```bash
git clone https://github.com/zsh-users/zsh-autosuggestions.git \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
**Uso:** Pressione → (seta para a direita) para aceitar a sugestão.

---

## zsh-completions
**Descrição:** Autocompletar avançado para centenas de ferramentas (docker, kubectl, git, etc.).  
**Instalação:**  
```bash
git clone https://github.com/zsh-users/zsh-completions.git \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-completions
```
**Uso:** Digite um comando e pressione **Tab** para ver opções.

---

## zsh-history-substring-search
**Descrição:** Busca no histórico por trechos de comando.  
**Instalação:**  
```bash
git clone https://github.com/zsh-users/zsh-history-substring-search.git \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-history-substring-search
```
**Uso:** Digite parte de um comando e use ↑/↓ para navegar apenas nos que contêm aquele trecho.

---

## fzf
**Descrição:** Buscador fuzzy poderoso para histórico e arquivos.  
**Instalação:**  
```bash
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install --all
```
**Uso:**  
- `Ctrl+R` → busca fuzzy no histórico  
- `Ctrl+T` → seleção fuzzy de arquivos  

---

## history
**Descrição:** Adiciona funções para manipular histórico.  
**Instalação:** Já incluso no Oh My Zsh.  
**Uso:**  
- `history -10` → mostra os últimos 10 comandos  
- `fc` → edita e repete comandos do histórico

---

## colored-man-pages
**Descrição:** Deixa os manuais (`man`) coloridos, destacando opções e seções.  
**Instalação:** Basta adicionar `colored-man-pages` na lista de plugins.  
**Uso:**  
```bash
man ls
```
O manual aparecerá com cores.

---

## extract
**Descrição:** Extrai qualquer arquivo compactado com um único comando.  
**Instalação:** Já incluso no Oh My Zsh.  
**Uso:**  
```bash
extract arquivo.zip
extract arquivo.tar.gz
```

---

## sudo
**Descrição:** Facilita repetir comandos com sudo.  
**Instalação:** Já incluso no Oh My Zsh.  
**Uso:**  
- `!!` → repete último comando  
- `sudo !!` → repete último comando com sudo

---

## encode64
**Descrição:** Codifica/decodifica Base64 direto no terminal.  
**Instalação:** Já incluso no Oh My Zsh.  
**Uso:**  
```bash
encode64 arquivo.txt
decode64 arquivo.b64
```

---

## dirhistory
**Descrição:** Navegação rápida entre diretórios com atalhos de teclado.  
**Instalação:** Já incluso no Oh My Zsh.  
**Uso:**  
- `Alt+←` → volta ao diretório anterior  
- `Alt+→` → avança ao próximo diretório

---

## safe-paste
**Descrição:** Evita execução acidental ao colar texto no terminal.  
**Instalação:** Já incluso no Oh My Zsh.  
**Uso:** Basta colar texto no terminal — o plugin impede execução imediata.

---

# Conclusão
Com esses plugins, o Zsh se torna uma ferramenta muito mais poderosa e segura para administrar servidores, editar arquivos, acompanhar logs e trabalhar com Git e pacotes.
```
