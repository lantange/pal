# pal
# Professional Assembly Language

# OS 
ubuntu-gnome-16.04-desktop-amd64
# Prerequisites
sudo apt install gcc-multilib

# Command
```bash
$ bash
# use as and ld
>>> as --32 -o xxx.o xxx.s
>>> ld -m elf_i386 -o xxx xxx.o
>>> ld -m elf_i386 -dynamic-linker /lib32/ld-linux.so.2 -o xxx xxx.o /lib32/libc.so.6
# use gcc
>>> sed -i 's/_start/main/g' xxx.s
>>> gcc -m32 -o xxx xxx.s
```
