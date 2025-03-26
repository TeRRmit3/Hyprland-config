Подключение к интеренету:
nmcli
nmcli device wifi list
nmcli device wifi connect "сеть" password "пароль"

Установка AUR:
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si

Установка шрифтов:
yay -S ttf-meslo-nerd-font-powerlevel10k
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

Установка,замена и настройка шела:
sudo pacman -S zsh
chsh:
/bin/zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
Плагины (автодополнение и подсветка синтаксиса):
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
  
Добавляем в .zshrc: ZSH_THEME="powerlevel10k/powerlevel10k"
plugins=(git z zsh-autosuggestions zsh-syntax-highlighting)
