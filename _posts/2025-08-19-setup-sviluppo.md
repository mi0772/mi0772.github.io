---
layout: post
title: "Configurare un ambiente di sviluppo moderno"
date: 2025-08-19 10:00:00 +0200
tags: [sviluppo, tools, setup]
---

In questo post voglio condividere la mia configurazione di sviluppo quotidiana, ottimizzata per produttività e semplicità.

## Editor: Neovim

La scelta dell'editor è fondamentale. Uso **Neovim** per la sua velocità e flessibilità:

```bash
# Installazione su macOS
brew install neovim

# Plugin manager: vim-plug
curl -fLo ~/.local/share/nvim/site/autoload/plug.vim --create-dirs \
  https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

## Terminal: iTerm2 + Oh My Zsh

Un terminale ben configurato fa la differenza:

- **iTerm2** per macOS
- **Oh My Zsh** per una shell più potente
- **Powerlevel10k** come tema

```bash
# Installare Oh My Zsh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# Installare Powerlevel10k
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

## Git: Configurazione essenziale

Alcune configurazioni Git che uso sempre:

```bash
git config --global user.name "Carlo"
git config --global user.email "carlo@example.com"
git config --global init.defaultBranch main
git config --global pull.rebase true
```

## Conclusioni

Una configurazione solida è la base per essere produttivi. Questi strumenti mi accompagnano ogni giorno e mi permettono di concentrarmi sul codice piuttosto che sui problemi tecnici.

Qual è la vostra configurazione preferita? Fatemi sapere nei commenti!
