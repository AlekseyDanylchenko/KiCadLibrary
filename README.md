# My KiCad Library

## Использование библиотеки в проекте.

В редакторе **pcbnew** зайдите в меню **Preferences -> Footprint Libraries Manager**
и добавьте библиотеку, заполнив поля следующим образом:

* Nickname = Baden_Github
* Library Path = https://github.com/baden/KiCadLibrary
* Plugin Type = Github

Чтобы использовать 3D-модели, загрузите их как описано в разделе **Загрузка 3d моделей**

## Загрузка 3d моделей.

Нужно загрузить каталог 3dshapes в рабочий каталог проекта (сохранив подкаталог 3dshapes).
Для этого зайдите в каталог с проектом и выполните в консоли команду:

```
svn checkout https://github.com/baden/KiCadLibrary/trunk/3dshapes && rm -rf 3dshapes/.svn
```

## Используемые инструменты и зависимости

* [OpenSCAD](http://www.openscad.org/)
* convert from ImageMagick

## Сборка 3d-моделей из исходников

Данный репозиторий используется как рабочая библиотека. Поэтому не забывайте перед публикацией изменений пересобирать модели.

```
    make
```

## Просмотр моделей в OpenSCAD

Список моделей можно посмотреть выполнив команду:

```
    make print-MODELS
```

Посмотреть модель в OpenSCAD можно выполнив

```
    make model-{Название модели}
```

например:

```
    make model-SIM800C
```

## Список моделей в библиотеке

1. SIM68 ![SIM68M](images/SIM68M.png)
2. SIM800C ![SI800C](images/SIM800C.png)
3. Inductor_NR6028T100M ![SI800C](images/Inductor_NR6028T100M.png)
4. MMA8452Q ![MMA8452Q](images/MMA8452Q.png)
5. FUSE_1812 ![FUSE_1812](images/FUSE_1812.png)
6. FUSE_1206 ![FUSE_1206](images/FUSE_1206.png)

Автоматичеки обновляемый [список инимированных моделей](List.md)

On-line [3D-модели](http://baden.github.io/KiCadLibrary/)
