# LunoOS-Main

## DISCLAIMER: OS is still under early development
Meaning: Things may not exist or work as expected

## How to build the ISO yourself
  - Update your system
    - sudo pacman -Syyu
  - Install needed packages
    - sudo pacman -S archiso
      - If you wish to test in a VM, you'll also need the qemu-desktop and edk2-ovmf
        packages

  - Build the ISO
    - sudo mkarchiso -v -w *path/to/work-dir* -o *path/to/output* *path/to/profile*
      - Note: It's recommended to set a working directory (directory where it's building the ISO), but it isn't really needed
      - e.g. : You've set the work-dir to *~/LunoOS-Work* , save it to your downloads (~/Downloads) and already cd'd into the Repository:
        - sudo mkarchiso -v -w ~/LunoOS-work -o ~/Downloads releng/

  - To test it in a VM:
      - run_archiso -u -i *path/to/ISO*/lunoOS-...-x86_64.iso

## Development Update (11.08.2025):
  - Successfully implemented Live-user (luno-live) for:
      - Autologin into KDE Plasma 6.x
      - Main installation process

  - Every following commit will go to an extra branch, which you should **not** use for building     the ISO!
      - If the changes there are in a stable state, they will be merged into the main branch

# ToDo-List:
  - Make a (flexible) installer with either bash or python
  - Include the option for a customized kernel during setup
