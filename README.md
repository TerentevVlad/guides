# Гайды по разработке

## Стандарты

* https://semver.org
* https://12factor.net/ru/
* https://nvie.com/posts/a-successful-git-branching-model/

## Использование зависимостей

Замечание по поводу хранения сторонних зависимостей в основном проекте. В частности Pod-ы для iOS.

Нам нужно придти к ситуации когда мы не храним Pod-ы (и любые другие зависимости) в репозитории основого проекта:

1) pod-ы живут своей жизнью, изменяются, обновляются и т.п. так или иначе 95% pod-ов публично доступны и развиваются.
2) занимает лишнее место в репозитории и новому входящему человеку не понятно: (то что лежит в Pods это что? что-то что само установилось через pod install? Тогда можно Pods грохнуть. Или это что-то что установили через pod install, потом пошли и ручками там в них что-то поменяли? Если поменяли то, что именно? Что случится если я обновлю версию pod, эти изменения потеряются или они уже лежат в исходном pod  и тп)
3) Одни и те-же pod-ы используются в разных проектах. Если хранить их копии в проектах то не понятно как их одновременно обслуживать и обновлять.

Поэтому:

1. Добавляем Pods в .gitignore: echo Pods >> .gitignore
2. Если что-то наменяли руками в Pods то выкатываем это на github отдельными проектами (публичными или форками уже существующих), если это так, то можно обсудить отдельно такие проекты. Подключаем такие pod-ы напрямую из github типа `pod 'SQLite.swift', :git => 'https://github.com/stephencelis/SQLite.swift.git', :branch => 'swift3-mariotaku'`
3. Удаляем из репозитория содержимое папки ./Pods: git rm -fr ./Pods/*; git commit -m 'Remove Pods/*';
4. Добавляем в папку .gitkeep чтобы сама папка осталась в проекте (а то git любит удалять пустые папки): `mkdir -f ./Pods; touch ./Pods/.gitkeep; git add -f ./Pods/.gitkeep; git commit -m 'Add Pods/.gitkeep'

Что касаемо Витрина плеер и других Pod-ов которых уже нет в живых. Делаем публичный репо в аккаунте https://github.com/limeHD/ (могу сделать я или Глеб, скажите только какое название) , копируем туда исходный код pod и подключаем его от туда в проект через  


PS Посмотрите на эталонные .gitignore для iOS разработки - https://www.gitignore.io/api/osx,swift,objective-c,xcode сделайте у себя такой-же, если что-то не вяжется - пишите.
