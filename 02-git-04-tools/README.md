1. Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea.
- commit aefead2207ef7e2aa5dc81a34aedf0cad4c32545
- comment: Update CHANGELOG.md

how: _git show aefea_

2. Какому тегу соответствует коммит 85024d3?
- tag: v0.12.23

how: _git show 85024d3_

3. Сколько родителей у коммита b8d720? Напишите их хеши.
- 2:
	- 56cd7859e05c36c06b56d013b55a252d0bb7e158 
	- 9ea88f22fc6269854151c571162c5bcf958bee2b

how: _git show b8d720 --pretty=format' %P'_

4. Перечислите хеши и комментарии всех коммитов которые были сделаны между тегами v0.12.23 и v0.12.24.
- _how: git log v0.12.23..v0.12.24 --oneline_
	- 33ff1c03b (tag: v0.12.24) v0.12.24
	- b14b74c49 [Website] vmc provider links
	- 3f235065b Update CHANGELOG.md
        - 6ae64e247 registry: Fix panic when server is unreachable
        - 5c619ca1b website: Remove links to the getting started guide's old location
        - 06275647e Update CHANGELOG.md
        - d5f9411f5 command: Fix bug when using terraform login on Windows
        - 4b6d06cc5 Update CHANGELOG.md
        - dd01a3507 Update CHANGELOG.md
        - 225466bc3 Cleanup after v0.12.23 release

5. Найдите коммит в котором была создана функция func providerSource, ее определение в коде выглядит так func providerSource(...) (вместо троеточего перечислены аргументы).
- 8c928e835 : Consult local directories as potential mirrors of providers

how: _git log --reverse --oneline -S 'func providerSource'_

6. Найдите все коммиты в которых была изменена функция globalPluginDirs.
how: _git log -S 'globalPluginDirs' --oneline_

- 35a058fb3 main: configure credentials from the CLI config file
- c0b176109 prevent log output during init
- 8364383c3 Push plugin discovery down into command package

7. Кто автор функции synchronizedWriters?
- Martin Atkins mart@degeneration.co.uk

how: _git log --pretty=format' %an' --reverse -S 'synchronizedWriters'_
