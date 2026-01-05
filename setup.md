# TAURCH

### Remove Packages
```bash
sudo pacman -Rs --noconfirm gnome-contacts gnome-weather gnome-maps snapshot yelp gnome-calculator gnome-calendar simple-scan gnome-text-editor epiphany malcontent showtime gnome-music papers gnome-software gnome-characters gnome-font-viewer
```

### Essential Packages
```bash
sudo pacman -S --noconfirm --needed base-devel wget curl p7zip kitty fzf fd ripgrep bob flatpak zathura zathura-pdf-poppler openssh gcc python make cmake nodejs npm rustup ttf-jetbrains-mono-nerd tree-sitter-cli pyright lua-language-server rust-analyzer tinymist typst uv gcc-fortran r  
```

### R Setup
```R
install.packages(c("tidyverse", "data.table", "janitor", "readxl", "openxlsx", "haven", "arrow", "lubridate", "fs", "here", "skimr", "ggthemes", "viridis", "patchwork", "modelr", "broom", "caret", "tidymodels", "rmarkdown", "knitr", "tinytex", "shiny", "roxygen2"))
```
