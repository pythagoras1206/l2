Что выведет программа? Объяснить вывод программы. Рассказать про внутреннее устройство слайсов и что происходит при передачи их в качестве аргументов функции.

```go
package main

import (
	"fmt"
)

func main() {
	var s = []string{"1", "2", "3"}
	modifySlice(s)
	fmt.Println(s)
}

func modifySlice(i []string) {
	i[0] = "3"
	i = append(i, "4")
	i[1] = "5"
	i = append(i, "6")
}
```

Ответ:
```
Вывод в консоль:
[3 2 3]
...
Мы можем модифицировать слайс при передачи в ф-цию modifySlice.

Модификация элемента по индексу: i[0] = "3". s и i все еще указывают на один и тот же слайс. Слайс s изменился.
ф-ция append создает новый слайс и присваевает его переменной i. s и i уже указывают на разые слайсы.
Модификация элемента по индексу: i[1] = "5". Слайс s не изменился.
ф-ция append создает новый слайс и присваевает его переменной i.

Вывод в консоль слайса s. 

```
