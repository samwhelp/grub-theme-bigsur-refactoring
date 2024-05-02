

# grub-theme-bigsur-refactoring

| Link | GitHub |
| ---- | ------ |
| [grub-theme-bigsur-refactoring](https://samwhelp.github.io/grub-theme-bigsur-refactoring/) | [GitHub](https://github.com/samwhelp/grub-theme-bigsur-refactoring) |
| [grub-theme-refactoring](https://samwhelp.github.io/grub-theme-refactoring) | [GitHub](https://github.com/samwhelp/grub-theme-refactoring) |
| [grub-theme-refactoring-select](https://samwhelp.github.io/grub-theme-refactoring-select/) | [GitHub](https://github.com/samwhelp/grub-theme-refactoring-select) |




## Subject

* [Theme Source](#theme-source)
* [Theme File](#theme-file)
* [Install](#install)
* [Apply](#apply)
* [Docs](#docs)




## Theme Source

| Theme Source |
| ------ |
| [Pling](https://www.pling.com/p/1443844/) |
| [GitHub](https://github.com/Teraskull/bigsur-grub2-theme) |





## Theme File

| Theme File                       |
| -------------------------------- |
| [theme.txt](theme.txt)           |
| [background.jpg](background.jpg) |




## Install

run

``` sh

mkdir -p "./tmp"

wget -c "https://github.com/samwhelp/grub-theme-bigsur-refactoring/archive/refs/heads/main.tar.gz" -O "./tmp/grub-theme-bigsur-refactoring-main.tar.gz"


tar xf "./tmp/grub-theme-bigsur-refactoring-main.tar.gz" -C "./tmp"


sudo mkdir -p "/boot/grub/themes"

sudo cp -rf "./tmp/grub-theme-bigsur-refactoring-main/." "/boot/grub/themes/grub-theme-bigsur-refactoring"

```

or run remote script [fetch.sh](https://github.com/samwhelp/grub-theme-bigsur-refactoring/blob/main/helper/theme-installer/fetch.sh)

``` sh
bash <(curl -L 'https://raw.githubusercontent.com/samwhelp/grub-theme-bigsur-refactoring/main/helper/theme-installer/fetch.sh')
```




## Apply

edit `/etc/default/grub`

```
GRUB_BACKGROUND='/boot/grub/themes/grub-theme-bigsur-refactoring/background.jpg'
GRUB_THEME="/boot/grub/themes/grub-theme-bigsur-refactoring/theme.txt"
```

or create file `/etc/default/grub.d/theme.cfg`, run

``` sh
cat << EOF | sudo tee /etc/default/grub.d/theme.cfg
GRUB_BACKGROUND='/boot/grub/themes/grub-theme-bigsur-refactoring/background.jpg'
GRUB_THEME="/boot/grub/themes/grub-theme-bigsur-refactoring/theme.txt"

EOF
```


then run

``` sh
sudo update-grub
```

or run

``` sh
sudo grub-mkconfig -o /boot/grub/grub.cfg
```




## Docs

| Grub Docs |
| ---- |
| [Theme file format](https://www.gnu.org/software/grub/manual/grub/html_node/Theme-file-format.html) |




## Styled Boxes

| Block          | Block      | Block          |
| ---------------| ---------- | -------------- |
| Northwest (nw) | North (n)  | Northeast (ne) |
| West (w)       | Center (c) | East (e)       |
| Southwest (sw) | South (s)  | Southeast (se) |
