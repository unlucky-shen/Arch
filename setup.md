# archlinux setup

### Nvidia Open Drivers

1. Enable `multilib` library at `/etc/pacman.conf`.

```bash
sudo pacman -S --noconfirm nvidia-open nvidia-utils lib32-nvidia-utils nvidia-settings nvidia-prime
```

### essentials
```bash
sudo pacman -S --noconfirm --needed base-devel wget curl p7zip kitty fzf fd ripgrep vim bob flatpak zathura zathura-pdf-poppler openssh gcc python make cmake nodejs npm rustup ttf-jetbrains-mono-nerd tree-sitter-cli pyright lua-language-server rust-analyzer tinymist typst uv gcc-fortran r eza swww
```

### Hyprland Packages
```bash
sudo pacman -S --noconfirm hyprland pipewire wireplumber hyprpolkitagent xdg-desktop-portal-hyprland qt5-wayland qt6-wayland xorg-xwayland waybar wofi dunst swww hyprsunset hypridle
```

### R packages
```R
install.packages(c("tidyverse", "data.table", "janitor", "readxl", "openxlsx", "haven", "arrow", "lubridate", "fs", "here", "skimr", "ggthemes", "viridis", "patchwork", "modelr", "broom", "caret", "tidymodels", "rmarkdown", "knitr", "tinytex", "shiny", "roxygen2"))
```
