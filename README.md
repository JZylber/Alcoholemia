# Estimador de Alcoholemia

## Consigna

Utilizando HTML y javascript, realizar una pequeña aplicación en donde el usuario pueda obtener su nivel de alcoholemia. El usuario debe ingresar el % de alcohol de la bebida y la cantidad de dicha bebida ingerida, y con esa información debe calcular la masa de alcohol ingerida. Recordemos cómo se calculaba:

1. Del volumen total de la consumición, tomamos el porcentaje de alcohol de la bebida y con eso calculamos el volumen de alcohol. Por ejemplo, en 500cc de una bebida de graduación de 50% hay 250cc de alcohol.
2. Tomamos el volumen de alcohol obtenido anteriormente, y con la densidad del etanol puro (0,789g/ml) obtenemos la masa (masa =  densidad x volumen).

Sin embargo, la gente no necesariamente sabe/recuerda los porcentajes de alcohol de determinadas bebidas. Para eso, vamos a incluir el porcentaje promedio de alcohol y el volumen de una consumición estándar de las bebidas que se encuentran en la siguiente [tabla](https://campus.ort.edu.ar/secundaria/belgrano/quimica/articulo/1127924/4-formas-de-expresar-concentracion-graduacion-alcoholica)

Como lo que importa es la alcoholemia, es decir, la concentración de alcohol etílico (etanol) en sangre, expresada cómo gramos de etanol por cada litro de sangre, necesitamos también los datos del cuerpo de la persona, en particular:

- El peso
- Sexo y tipo de cuerpo (para obtener los coeficientes se encuentran en este [link](https://campus.ort.edu.ar/secundaria/belgrano/quimica/articulo/1127949/alcoholemia-concentracion-de-alcohol-en-sangre)). **No puede ser simplemente exponer la información, la aplicación debe tener una forma de ingresar esta información de forma automática, eligiendo de opciones**.

Con esta información, se debe calcular la alcoholemia. Con el peso y el coeficiente (R), calculan los litros de sangre en el organismo, y la alcholemia es la masa dividida este total: alcoholemia = masa_etanol / (R x peso).

Además, queremos incluir el factor tiempo, para tener en cuenta la eliminación del etanol con el tiempo. Esto es útil si por ejemplo queremos estimar el tiempo hasta tener un nivel legal para manejar (**¡Recuerden que es sólo una estimación!**). Para eso, debemos pedirle al usuario el tiempo desde consumido. Usando a que la alcoholemia desciende 0.15 g/L por hora que transcurre, modificar el cálculo de la alcoholemia tomando en cuenta esta eliminación.

Por último, nos interesa también informar las consecuencias de ese nivel de alcoholemia, por ejemplo, si usamos la app para estimar consumos futuros. Calculada la alcoholemia, exponer en el html el estado dado el nivel calculado. Saquen la información de esta [página](https://campus.ort.edu.ar/secundaria/belgrano/quimica/articulo/1128361/6-alcoholemia-y-efectos-en-nuestro-organismo).

Dados estos lineamientos generales, la aplicación debe cumplir:

- Capacidad de ingresar manualmente el porcentaje de alcohol y el volumen de consumición.
- Una forma de acceder al porcentaje de alcohol y consumición estándar de las bebidas provistas. **No alcanza simplemente con poner la información, debe haber un mecanismo de relleno automático al elegir una bebida**.
- Capacidad de ingresar manualmente el peso.
- Capacidad de elegir sexo y tipo de cuerpo de forma independiente.
- Validación de los valores ingresados, no simplemente calcular y devolver resultados erróneos. En particular:
  - Asegurarse que haya valores de porcentaje de alcohol y valor consumido.
  - Asegurarse que el porcentaje de alcohol sea un número entre 0 y 100, permitiendo hasta 1 cifra decimal.
  - (Depende de la implementación) Asegurarse que la bebida elegida sea una de las bebidas de las que contamos con información.
  - Asegurarse haya valores de peso válidos (mayores a 0).
  - Asegurarse que haya valores de sexo y tipo de cuerpo.
  - La combinación sexo-tipo de cuerpo debe ser una de las combinaciones de la tabla.
- El resultado debe  aparecer por html, no por consola ni por alerta.

Para hacerlo más prolijo, se sugiere editar el css para que la interfaz sea más clara. No es obligatorio igual, puede quedar simplemente el HTML y Javascript en archivos separados.

## Extras

Como siempre, pueden sumar puntos a la nota del trabajo haciendo alguno de los extras sugeridos:
- (hasta 2 puntos) Agregarle diseño y color con css a la página. Flex y Grid son herramientas muy útiles, dejo un tutorial/juego para aprender cada uno:
  - [Flexbox Froggy](https://flexboxfroggy.com/) (para aprender flexbox)
  - [Grid Garden](https://cssgridgarden.com/) (para aprender grid)
- (1 punto) Calcular el tiempo aproximado para estar debajo del límite legal argentino. Pueden permitirle al usuario otro nivel de alcoholemia, ya sea por que se puede usar en otros países, o porque desea el tiempo estimado para llegar a ese grado de alcoholemia.
- (hasta 2 puntos) Capacidad de ingresar múltiples bebidas. Además, pueden dar la opción de ver que bebidas fueron ingresando, pudiendo modificar o eliminarlas.

También cualquier otro extra que se les ocurra y conversado previamente conmigo.

## Entrega
Hacen push en el repositorio de su grupo y suben el hash del commit al campus con todos los miembros del grupo.