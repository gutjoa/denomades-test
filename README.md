# Denomades Test

## Requerimiento

Los destinos deben mostrar los siguientes datos:
- Nombre
- Imagen thumbnail
- URL

Las actividades deben mostrar los siguientes datos:
- Nombre
- Imagen thumbnail
- URL
- Precio base
- Descripción corta

Otros aspectos a tomar en cuenta:
- Los datos de las actividades deben ser cargados en múltiples idiomas (español, inglés y portugués).
- Las actividades publicadas en la landing page pueden tener la tarifa cargada en USD o CLP.
- La landing page debe tener la opción de convertir todos los precios de las actividades a USD o CLP.
- Si bien el evento dura tres días, algunas actividades y/o destinos estarán en oferta solo durante el primer día.
- Cada destino debe mostrar un contador que indique cuántas actividades hay en oferta.
- Es necesario conocer el precio anterior de la actividad junto al porcentaje de descuento.

## Solución

### Gráfico

[![](https://mermaid.ink/img/eyJjb2RlIjoiY2xhc3NEaWFncmFtXG4gICAgRGVzdGlueSBcIm9uZVwiIC0tIFwibWFueVwiIEFjdGl2aXR5XG4gICAgQWN0aXZpdHkgXCJvbmVcIiAtLSBcIm1hbnlcIiBQcmljZVxuICAgIEFjdGl2aXR5IFwib25lXCIgLS0gXCJtYW55XCIgRGVzY3JpcHRpb25cbiAgICBQcmljZSBcIm1hbnlcIiAtLSBcIm9uZVwiIENvaW5fdHlwZVxuICAgIERlc2NyaXB0aW9uIFwibWFueVwiIC0tIFwib25lXCIgTGFuZ3VhZ2VcbiAgICBjbGFzcyBEZXN0aW55IHtcbiAgICAgICAgK2ludGVnZXI6IGlkXG4gICAgICAgICtzdHJpbmc6IG5hbWVcbiAgICAgICAgK3N0cmluZzogaW1hZ2VfdGh1bWJuYWlsXG4gICAgICAgICt0ZXh0OiB1cmxcbiAgICAgICAgK2ludGVnZXI6IGRpc2NvdW50XG4gICAgICAgICtkYXRldGltZTogZGlzY291bnRfZGF0ZVxuICAgICAgICArZGF0ZXRpbWU6IGRhdGVfaW5pdFxuICAgICAgICArZGF0ZXRpbWU6IGRhdGVfZmluaXNoXG4gICAgICAgICtnZXRDb3VudFRvdGFsQWN0aXZpdHkoaWQpIGludFxuICAgIH1cbiAgICBjbGFzcyBBY3Rpdml0eSB7XG4gICAgICAgICtpbnRlZ2VyOiBpZFxuICAgICAgICArdGV4dDogdXJsXG4gICAgICAgICtpbnRlZ2VyOiBkaXNjb3VudFxuICAgICAgICArZGF0ZXRpbWU6IGRpc2NvdW50X2RhdGVcbiAgICAgICAgK2RhdGV0aW1lOiBkYXRlX2luaXRcbiAgICAgICAgK2RhdGV0aW1lOiBkYXRlX2ZpbmlzaFxuICAgICAgICArZ2V0UHJpY2UoYWN0aXZpdHlfaWQpIGFycmF5XG4gICAgICAgICtnZXREZXNjcmlwdGlvbihkZXNwcmlwdGlvbl9pZCkgYXJyYXlcbiAgICB9XG4gICAgXG4gICAgY2xhc3MgUHJpY2Uge1xuICAgICAgICAraW50ZWdlcjogaWRcbiAgICAgICAgK2ludGVnZXI6IHZhbHVlXG4gICAgICAgICtpbnRlZ2VyOiBhY3Rpdml0eV9pZFxuICAgICAgICAraW50ZWdlcjogY29pbl90eXBlX2lkXG4gICAgfVxuICAgIGNsYXNzIENvaW5fdHlwZSB7XG4gICAgICAgICtpbnRlZ2VyOiBpZFxuICAgICAgICArc3RyaW5nOiBuYW1lXG4gICAgICAgICtzdHJpbmc6IHNob3J0X25hbWVcbiAgICAgICAgK2ludDogc3RhdHVzXG4gICAgfVxuICAgIGNsYXNzIERlc2NyaXB0aW9ue1xuICAgICAgICAraW50ZWdlcjogaWRcbiAgICAgICAgK3RleHQ6IHZhbHVlXG4gICAgICAgICt0ZXh0OiBzaG9ydF92YWx1ZVxuICAgICAgICAraW50ZWdlcjogYWN0aXZpdHlfaWRcbiAgICAgICAgK2ludGVnZXI6IGxhbmd1YWdlX2lkXG4gICAgfVxuICAgIGNsYXNzIExhbmd1YWdlIHtcbiAgICAgICAgK2ludGVnZXI6IGlkXG4gICAgICAgICtzdHJpbmc6IG5hbWVcbiAgICAgICAgK3N0cmluZzogc2hvcnRfbmFtZVxuICAgICAgICAraW50ZWdlcjogc3RhdHVzXG4gICAgfVxuICAgICAgICAgICAgIiwibWVybWFpZCI6e30sInVwZGF0ZUVkaXRvciI6ZmFsc2V9)](https://mermaid-js.github.io/mermaid-live-editor/#/edit/eyJjb2RlIjoiY2xhc3NEaWFncmFtXG4gICAgRGVzdGlueSBcIm9uZVwiIC0tIFwibWFueVwiIEFjdGl2aXR5XG4gICAgQWN0aXZpdHkgXCJvbmVcIiAtLSBcIm1hbnlcIiBQcmljZVxuICAgIEFjdGl2aXR5IFwib25lXCIgLS0gXCJtYW55XCIgRGVzY3JpcHRpb25cbiAgICBQcmljZSBcIm1hbnlcIiAtLSBcIm9uZVwiIENvaW5fdHlwZVxuICAgIERlc2NyaXB0aW9uIFwibWFueVwiIC0tIFwib25lXCIgTGFuZ3VhZ2VcbiAgICBjbGFzcyBEZXN0aW55IHtcbiAgICAgICAgK2ludGVnZXI6IGlkXG4gICAgICAgICtzdHJpbmc6IG5hbWVcbiAgICAgICAgK3N0cmluZzogaW1hZ2VfdGh1bWJuYWlsXG4gICAgICAgICt0ZXh0OiB1cmxcbiAgICAgICAgK2ludGVnZXI6IGRpc2NvdW50XG4gICAgICAgICtkYXRldGltZTogZGlzY291bnRfZGF0ZVxuICAgICAgICArZGF0ZXRpbWU6IGRhdGVfaW5pdFxuICAgICAgICArZGF0ZXRpbWU6IGRhdGVfZmluaXNoXG4gICAgICAgICtnZXRDb3VudFRvdGFsQWN0aXZpdHkoaWQpIGludFxuICAgIH1cbiAgICBjbGFzcyBBY3Rpdml0eSB7XG4gICAgICAgICtpbnRlZ2VyOiBpZFxuICAgICAgICArdGV4dDogdXJsXG4gICAgICAgICtpbnRlZ2VyOiBkaXNjb3VudFxuICAgICAgICArZGF0ZXRpbWU6IGRpc2NvdW50X2RhdGVcbiAgICAgICAgK2RhdGV0aW1lOiBkYXRlX2luaXRcbiAgICAgICAgK2RhdGV0aW1lOiBkYXRlX2ZpbmlzaFxuICAgICAgICArZ2V0UHJpY2UoYWN0aXZpdHlfaWQpIGFycmF5XG4gICAgICAgICtnZXREZXNjcmlwdGlvbihkZXNwcmlwdGlvbl9pZCkgYXJyYXlcbiAgICB9XG4gICAgXG4gICAgY2xhc3MgUHJpY2Uge1xuICAgICAgICAraW50ZWdlcjogaWRcbiAgICAgICAgK2ludGVnZXI6IHZhbHVlXG4gICAgICAgICtpbnRlZ2VyOiBhY3Rpdml0eV9pZFxuICAgICAgICAraW50ZWdlcjogY29pbl90eXBlX2lkXG4gICAgfVxuICAgIGNsYXNzIENvaW5fdHlwZSB7XG4gICAgICAgICtpbnRlZ2VyOiBpZFxuICAgICAgICArc3RyaW5nOiBuYW1lXG4gICAgICAgICtzdHJpbmc6IHNob3J0X25hbWVcbiAgICAgICAgK2ludDogc3RhdHVzXG4gICAgfVxuICAgIGNsYXNzIERlc2NyaXB0aW9ue1xuICAgICAgICAraW50ZWdlcjogaWRcbiAgICAgICAgK3RleHQ6IHZhbHVlXG4gICAgICAgICt0ZXh0OiBzaG9ydF92YWx1ZVxuICAgICAgICAraW50ZWdlcjogYWN0aXZpdHlfaWRcbiAgICAgICAgK2ludGVnZXI6IGxhbmd1YWdlX2lkXG4gICAgfVxuICAgIGNsYXNzIExhbmd1YWdlIHtcbiAgICAgICAgK2ludGVnZXI6IGlkXG4gICAgICAgICtzdHJpbmc6IG5hbWVcbiAgICAgICAgK3N0cmluZzogc2hvcnRfbmFtZVxuICAgICAgICAraW50ZWdlcjogc3RhdHVzXG4gICAgfVxuICAgICAgICAgICAgIiwibWVybWFpZCI6e30sInVwZGF0ZUVkaXRvciI6ZmFsc2V9)

### Descripción del gráfico
En el siguiente gráfico se definieron las clases principales:

- Destiny (Destino)
- Activity (Actividades)
- Price (precios)
- Description (descripción)
- Coin_type (tipo de moneda)
- Language (Idioma)

Dentro de la tabla destino cuenta con los campos id como identificador, nombre, imagen, url, discount campo numérico que guarda el valor del descuento, discount_date es la fecha en la cual terminara el descuento que se de al destino  y 2 campos tipo fecha los cuales será para el inicio y fin, que permite controlar la visualización, también tendrá una función la cual devolverá un valor numero con la cantidad de actividades que cuenta.

Dentro de la tabla activity, cuenta con el campo id como identificador, url, discount campo numero que guardara el valor de descuento, discount_date es la fecha en la cual terminara el descuento que se de a la actividad , también tendrá fecha de inicio y fin de manera de poder verificar por medio de las fechas su visualización. También tendrá 2 funciones las cuales traerán en un array los precios o valores de esta actividad y las descripciones en distinto idioma.

Dentro de la tabla coin_type, cuent con el campo id como identificador, name el nombre de la moneda y short_name que será la forma corta y status que nos permitirá saber si se muestra o no el tipo de moneda, esta tabla se utiliza para definir los tipos de monedas, como en este caso serian `[{name: "Dolar Americano", short_name: "USD"}, {name: "Pesos Chilenos", tag: "CLP"}]` esta tabla será la referencia en el sitio para poder realizar cambios de moneda.

Dentro de la tabla language, cuenta con el campo id como identificador, name el nombre del idioma y short_name que es la forma corta del idioma, esta tabla alojara todos los idiomas en los cuales soportara los textos del sitio web, para este caso serian `[{name:"Español", short_name: "ES"}, {name:"Inglés", short_name: "EN"}, {name:"portugués", short_name: "PT"}]`

Dentro de la tabla price, cuanta con los campos id como identificador, value que es el valor monetario, activity_id viene a ser la relación con la actividad y coin_type_id es la relación que tiene con el tipo de moneda. 


Dentro de la tabla description, cuenta con los campos id como identificador, value es el la descripción completo de la actividad, short_value el una descripción breve de la actividad, activity_id es la relación o a la actividad que pertenece y language_id es la relación con la tabla language, la que nos permitirá saber el idioma de la descripción

Dentro del modelo, en las tablas Destino y Actividad su visualización esta centrada en las fechas de inicio, fin y descuento, de esta manera este modelo puede ser reutilizado en siguientes eventos los cuales mantenga los mismo requerimientos, adicional que solo el cambio para otros eventos se encontraría en el front.

### Aspectos solicitados

- Los datos de las actividades deben ser cargados en múltiples idiomas (español, inglés y portugués).
> El modelo que se presenta podrá tomar los 3 idiomas solicitados y a su vez si a futuro se agrega otro también será soportado.
  
- Las actividades publicadas en la landing page pueden tener la tarifa cargada en USD o CLP.
> EL modelo que se presenta puede trabajar con ambas monedas y se le podrá agregar otras si a futuro es necesario.
  
- La landing page debe tener la opción de convertir todos los precios de las actividades a USD o CLP.
> Al tener la tabla separada, permite llamarla en el landing page de manera de tener los identificadores y poder hacer un filtro según sea el tipo de moneda, así poder mostrar la selección.

- Si bien el evento dura tres días, algunas actividades y/o destinos estarán en oferta solo durante el primer día.
> Dentro del modelo, se define 2 campos que son discount y discount_date, en los cuales se definirá el valor de descuento y los días o la fecha que finaliza el descuento, dado que tiene la fecha de inicio se puede controlar cuando se deja de visualizar en el landing page.

- Cada destino debe mostrar un contador que indique cuántas actividades hay en oferta.
> Dentro del modelo, se define una función la cual entregue el valor total de las actividades relacionadas a cada destino.
  
- Es necesario conocer el precio anterior de la actividad junto al porcentaje de descuento.
> El campo discount es el valor de descuento, teniendo ya los valores iniciales en price, por medio de un calculo matemático se podrá tener el valor de descuento, de esta manera ambos valores pueden ser mostrados sin problemas.


