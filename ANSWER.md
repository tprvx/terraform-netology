1. commit aefead2207ef7e2aa5dc81a34aedf0cad4c32545
Author: Alisdair McDiarmid <alisdair@users.noreply.github.com>
Date:   Thu Jun 18 10:29:58 2020 -0400

    Update CHANGELOG.md

2. Ответы:
 - Какому тегу соответствует коммит 85024d3?
	tag: v0.12.23

 - Сколько родителей у коммита b8d720?
 	```Bash
 		git show b8d720
 		git show b8d720^1
 		git show b8d720^2
 	```
 	2 родителя:
 		56cd7859e05c36c06b56d013b55a252d0bb7e158
 		9ea88f22fc6269854151c571162c5bcf958bee2b

  - Перечислите хеши и комментарии всех коммитов, которые были сделаны между тегами v0.12.23 и v0.12.24:
  	```Bash
  		git log --oneline v0.12.23 v0.12.24 -20
  	```
  	33ff1c03bb (tag: v0.12.24) v0.12.24

	b14b74c493 [Website] vmc provider links
	3f235065b9 Update CHANGELOG.md
	6ae64e247b registry: Fix panic when server is unreachable
	5c619ca1ba website: Remove links to the getting started guide's old location
	06275647e2 Update CHANGELOG.md
	d5f9411f51 command: Fix bug when using terraform login on Windows
	4b6d06cc5d Update CHANGELOG.md
	dd01a35078 Update CHANGELOG.md
	225466bc3e Cleanup after v0.12.23 release

	85024d3100 (tag: v0.12.23) v0.12.23

 - Найдите коммит, в котором была создана функция func providerSource:
 	8c928e8358 main: Consult local directories as potential mirrors of providers
 	```Bash
 		git log -S"func providerSource(" --oneline
 	```

 - Найдите все коммиты, в которых была изменена функция globalPluginDirs:
	```Bash
		git log -L :globalPluginDirs:plugins.go
	```
	8364383c35 Push plugin discovery down into command package
	66ebff90cd move some more plugin search path logic to command
	41ab0aef7a Add missing OS_ARCH dir to global plugin paths
	52dbf94834 keep .terraform.d/plugins for discovery
	78b1220558 Remove config.go and update things using its aliases

 - Кто автор функции synchronizedWriters:
 	```Bash
		git log -SsynchronizedWriters --oneline
		git show 5ac311e2a9
	```
	Author: Martin Atkins <mart@degeneration.co.uk>


 	


