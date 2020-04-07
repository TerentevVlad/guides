# Что требуется от README проекта

## Для кого пишутся README? 

README пишутся для пользователей Вашего изделия. Пользователем является любой человек который каким-то образом использует Ваше изделие и заглядывает в репозиторий. Как правило пользователи бывают такие:

1. Новый разработчик, который перенимает Ваш проект после Вас или подключается в него дополнительно.
2. Тестировщик, который разворачивает этот проект у себя на компьютере чтобы в него потыкать.
3. sysadmin, sysop, devops - люди которые разворачивают этот проект на серверах и должны понимать как это делать.

## Критерий качественного README

Пользователь БЕЗ непосредственного обращения к разработчику, БЕЗ затрачивания времени на изучение и решение проблем может: развернуть проект для разработки, внести в него изменения, запустить в боевом и тестовом окружении на сервере.

## Типовая структура README

1. Краткое описание зачем нужен этот проект, кто его заказал и для чего.
1. Бейджи на билд мастера на CI
1. Как развернуть рабочее окружение и зависимости проекта для разработки (раздел Dependencies)
1. Как сбилдить и запустить проект для разработки (раздел Development)
1. Как запустить в проекте тесты (раздел Testing)
1. Какие настройки и конфигуарция есть в проектк и как их спользовать (раздел Settings)
1. Как запускать проект в рабочем окруженеии (раздел Production)
1. Как развернуть проект на боевом сервере (раздел Deploy). Обычно тут будет что-то типа `cap production deploy`. За этот раздел отвечает devops.
1. Ссылки и аватарки на авторов, контрибьютеров и майнтейнеров проекта.

## Пример README

В поиске