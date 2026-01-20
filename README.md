## Setup auto-cpufreq
```bash
# Install & Setup
git clone https://github.com/AdnanHodzic/auto-cpufreq.git
cd auto-cpufreq && sudo ./auto-cpufreq-installer

# Enable
sudo auto-cpufreq --install
```

# Nvidia tweaks

1. Install necessary packages,

```bash
sudo pacman -S --noconfirm nvidia nvidia-utils nvidia-settings nvidia-prime
```

2. Append parameters on `options` line in `/boot/loader/entries/arch.conf`

```arch.conf
options root=UUID=... rw nvidia-drm.modeset=1 nvidia-drm.fbdev=1
```

3. Create Modprobe configuration (`/etc/modprobe.d/nvidia.conf`)
``` nvidia.conf
options nvidia-drm modeset=1
options nvidia NVreg_DynamicPowerManagement=0x02
```

4. Enable NVIDIA Services,
```bash
sudo systemctl enable nvidia-suspend.service
sudo systemctl enable nvidia-hibernate.service
sudo systemctl enable nvidia-resume.service
```

5. Edit `/etc/mkinitcpio.conf` for early loading,
```mkinitcpio.conf
MODULES=(nvidia nvidia_modeset nvidia_uvm nvidia_drm)
```

and then, regenerate initramfs,
```bash
sudo mkinitcpio -P
```
