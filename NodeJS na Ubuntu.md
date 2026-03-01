## Koraci:
1. Otvori terminal
2. Kopiraj: `sudo apt install curl`, pa Enter
3. Kopiraj: `sudo apt update && sudo apt upgrade -y && sudo apt autoremove -y`, pa Enter
4. Kopiraj: `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash`, pa Enter
5. Kopiraj: `export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm`, pa Enter
6. Verifikuj nvm: `command -v nvm`, pa Enter
7. Kopiraj: `nvm install --lts`, pa Enter
8. Kopiraj: `nvm use --lts`, pa Enter
## Korišćenje:
U terminalu kucati `node`, pa Enter; a za izlazak kucati `.exit`, pa Enter




