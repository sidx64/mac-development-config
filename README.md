# mac-development-config

My configuration files for setting up the tastiest development setup on a mac - now with Big Sur in mind

# Before you begin:

0.  Install XCode Command line tools

        sudo rm -rf /Library/Developer/CommandLineTools
        sudo xcode-select --install

1.  Install Homebrew

        /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

2.  Install the Brewfiles Cask

        brew tap Homebrew/bundle

3.  Install ohmyzsh

        sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

4.  Configure ownership of some directories to avoid issues (replace <USER> with your username)

        sudo chown <USER> ~/.config

5.  Run brew bundle command in the same directory as the brewfile

        brew bundle

6.  Replace the .zshrc file in home directory with the one provided in this repo

        cp zsh-config/zshrc ~/.zshrc

7.  Install the versions of python you want

        pyenv install 3.8.6
        pyenv install 3.9.1

8.  Restart the shell and make sure no errors or warnings pop up.

9.  VS Code Extension installations - [DO NOT RUN if using VSCode Settings Sync]
    Run the following commands:

        code --install-extension ritwickdey.liveserver
        code --install-extension esbenp.prettier-vscode
        code --install-extension ms-python.python
        code --install-extension dbaeumer.vscode-eslint
        code --install-extension visualstudioexptteam.vscodeintellicode
        code --install-extension vscode-icons-team.vscode-icons
        code --install-extension ms-toolsai.jupyter
        code --install-extension redhat.vscode-yaml
        code --install-extension ecmel.vscode-html-css
        code --install-extension davidanson.vscode-markdownlint
        code --install-extension alefragnani.project-manager
        code --install-extension formulahendry.terminal
        code --install-extension ms-vscode.atom-keybindings
        code --install-extension formulahendry.auto-rename-tag
        code --install-extension amazonwebservices.aws-toolkit-vscode
        code --install-extension streetsidesoftware.code-spell-checker
        code --install-extension anseki.vscode-color
        code --install-extension kamikillerto.vscode-colorize
        code --install-extension pranaygp.vscode-css-peek
        code --install-extension danields761.dracula-theme-from-intellij-pythoned
        code --install-extension msjsdiag.debugger-for-chrome
        code --install-extension firefox-devtools.vscode-firefox-debug
        code --install-extension msjsdiag.debugger-for-edge
        code --install-extension ms-azuretools.vscode-docker
        code --install-extension mikestead.dotenv
        code --install-extension dsznajder.es7-react-js-snippets
        code --install-extension donjayamanne.githistory
        code --install-extension github.vscode-pull-request-github
        code --install-extension wix.vscode-import-cost
        code --install-extension xabikos.javascriptsnippets
        code --install-extension ms-vscode.js-debug-nightly
        code --install-extension ms-vsliveshare.vsliveshare
        code --install-extension ms-vsliveshare.vsliveshare-audio
        code --install-extension magicstack.magicpython
        code --install-extension shd101wyy.markdown-preview-enhanced
        code --install-extension teamsdevapp.ms-teams-vscode-extension
        code --install-extension hookyqr.minify
        code --install-extension eg2.vscode-npm-script
        code --install-extension christian-kohler.npm-intellisense
        code --install-extension christian-kohler.path-intellisense
        code --install-extension ms-vscode-remote.remote-containers
        code --install-extension humao.rest-client
        code --install-extension jasonnutter.search-node-modules
        code --install-extension fabiospampinato.vscode-todo-plus
        code --install-extension eighthundreds.vscode-drawio
        code --install-extension blanu.vscode-styled-jsx

# Attributions

## Fonts

- Fira Flott - https://github.com/kosimst/FiraFlott/tree/master/TTF
- Input Font - https://input.fontbureau.com/
- Fira Code - https://github.com/tonsky/FiraCode
- Powerline Fonts - https://github.com/powerline/fonts
- iterm2 color schemes - https://iterm2colorschemes.com/
