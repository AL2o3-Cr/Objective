<meta charset="UTF-8">
<meta lang="RU">

# Язык UniJect

Самое важное - это изменение синтаксиса прямо в процессе выполнения программы

Пример: игнориравание участка обрамлёного `#`.  
```
:ignore #id ситаксиса для обращения к нему в дальнейшем.#
\#0..0\#0; #`0` оканчание фрагмента ситаксиса. `..0` - что-либо.  `;` - заканчивает синтаксис#
:ignore #действие синтаксиса# 
```
```
:Decl
!class0 0!name0; #`!class0` это применение формы class, при этом `!` означает жёсткость применения#
class=~name,=Decled #определение формы class, `~name` - не чёткое применение формы, `=Decled` уже обьявленный обьект#
name=[byte] #определение формы name как набор символов кодировки UTF-8#
:Decl #обьявление нового обьекта#
```



## Программа на *UniJect* состоит из объектов.

Объект класса `UJ` может быть функцией, хранилещем данных и классом, а также абстракцией (классом классов).  
Выполняемая программа то же является обектом.

В любой объект встроенна `obj.__G` 

## Встроенное :
### Ситаксис :
```
:Ignore
\#0..0\#0;
:Ignore
```
```
:DeclNewNonClass
!name0;
name=[byte]
:DeclNew
```
```
:DeclFromFile
from 0!from0 as 0!name0;
from=FilePuth,=FromModules
name=[byte]
:DeclFromFile
```
```
:DeclIn
!class0&0!name0;
:DeclIn
```

### Классы :
* `uj`
* `arr` - индексированый набор конечных данных
* `bit`
* `byte`
* `count`
### Функиции :
* `ifs(bit$cond, uj$true,\ uj$false);`
* `while(bit$cond, uj$true,\ uj$finally);`
* `foreach(uj$code, arr || byte || uj,\ uj$finally);`
* `switch(uj$var, uj$answers,\ uj$false);`
---
