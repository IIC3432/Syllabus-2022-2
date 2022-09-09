## Experiencia de laboratorio. 

Para esta experiencia debes tener un computador con: 
- Redis, en donde el módulo redisbloom este operativo
- Algún lenguaje de programación que interactue con Redis. 

### Software

Instrucciones para [Redis](https://redis.io/docs/getting-started/) y para [RedisBloom](https://redis.io/docs/stack/bloom/quick_start/). Yo no tengo docker pero me funcionó perfecto construirlo desde el repo. 
Python tiene la libreria [Redis](https://redis.readthedocs.io/en/stable/index.html), que supuestamente soporta redisbloom también, pero a mi solo me funcionó instalando ademas [redisbloom-py](https://github.com/RedisBloom/redisbloom-py)

**Importante**. Para asegurar que todo está bien, intenta crear un filtro de bloom y meter un par de numeros antes del martes. 


### Actividad. 

1.- Crea un filtro de bloom que garantize tasa de error 0.01 para 10.000 elementos. Agregale 5000 elementos, luego prueba 5000 que no están para tomar un estimado de la tasa de error. Ahora agregale otros 5000, y vuelve a estimar el error. ¿Qué concluyes?

2.- Averigua un poco sobre Cuckoo Filters. ¿En que se diferencian de los de Bloom?

3.- Puedes Usar Memory Usage (memory_usage en python) para ver cuanta memoria está usando un filtro. Observa como crece la memoria que necesita un filtro de Bloom o de Cuckoo según numero de entradas, manteniendo el error en 0.01. 

4.- Crea un Count-min sketch, para una cantidad de entradas y de hashes que definas tu. Con este sketch, alimentalo de elementos de forma que puedas ir viendo qué pasa con las estimaciones. 

5.- Diseña un experimento que de cuenta de la relación entre el rango de error empírico que te entrega el count-min sketch y el aumento de el conteo de algunos o de todos los elementos. 
