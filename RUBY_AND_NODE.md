# Подготовка к работе с ruby и nodejs

Предварительно устновите из под рута в систему часто требуемые пакеты из [списка](https://github.com/LimeHD/ansible/blob/master/ruby.yml#L10-L20)

## Установите и настройте `rbenv` и `rbenv-build` локально (не из под рута, а домашний каталог)

Если вы все настроили правильно, то при смене текущего каталога в shell, будет меняться версия руби на ту, которая указана в файле `.ruby-version`

```
> echo 2.7.0 > .ruby-version
> ruby -v
ruby 2.7.0
```

## Также локально установите `nvm`