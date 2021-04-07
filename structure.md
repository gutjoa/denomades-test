### Estrutura de Diagrama de Clases en mermaind

```ssh
classDiagram
    Destiny "one" -- "many" Activity
    Activity "one" -- "many" Price
    Activity "one" -- "many" Description
    Price "many" -- "one" Coin_type
    Description "many" -- "one" Language
    class Destiny {
        +integer: id
        +string: name
        +string: image_thumbnail
        +text: url
        +integer: discount
        +datetime: discount_date
        +datetime: date_init
        +datetime: date_finish
        +getCountTotalActivity(id)
        +getActivity(activity_id, language_id)
    }
    class Activity {
        +integer: id
        +text: url
        +integer: discount
        +integer: destiny_id
        +datetime: discount_date
        +datetime: date_init
        +datetime: date_finish
        +getPrice(activity_id, coin_type_id) 
        +getDescription(despription_id, language_id) 
    }
    
    class Price {
        +integer: id
        +integer: value
        +integer: activity_id
        +integer: coin_type_id
    }
    class Coin_type {
        +integer: id
        +string: name
        +string: short_name
        +int: status
    }
    class Description{
        +integer: id
        +string: title
        +text: value
        +text: short_value
        +integer: activity_id
        +integer: language_id
    }
    class Language {
        +integer: id
        +string: name
        +string: short_name
        +integer: status
    }
            
                
```  
