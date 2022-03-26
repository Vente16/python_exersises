# python exersises

``` Python

# Ejercicio 1:
def funct_size_num(_num):
    return len(str(_num)) if type(_num) is int and _num > 0 else "el valor debe ser un número positivo"

# Ejercicio 2 (recursividad) 
# Comparar posiciones 
# Profe! por favor ayúdame aquí, no sé qué hacer :'( 
def func_compare(_value, _list, _from = 0, count = 0):
    _size = len(_list)
    if _from < _size:
        if _value >= _list[_from]:
           count+=1
           if count == _size and _value is not None:
              print('El valor máximo es:', _value)
        _from+=1
        func_compare(_value, _list, _from, count)
        
# function principal recursiva para cada item
def func_max_(_list, _i = 0):
    if type(_list) is not list:
       print("Upps! así no puede funcionar :/")
       return False
     
    _size_list = len(_list)
    if _i < _size_list:
        _get_max = func_compare (_list[_i], _list)
        _i+=1
        func_max_(_list, _i)

# Ejercicio 1
print("El número de digitos es de:", funct_size_num(5634343))

# Ejericio 2
_my_list = [2, 50, 250, 100, 10, 39, 5]
func_max_(_my_list)

```
