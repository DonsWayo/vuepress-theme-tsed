# Converters

The Converters service is responsible for serializing and deserializing objects.

It has two modes of operation:

- The first uses the [class models](/docs/model.md) for
  convert an object into a class (and vice versa).
- The second is based on the JSON object itself to provide an object with the right types. For example the deserialization of dates.


The Converters service is used by the following decorators:
<ul class="api-list"><li class="api-item" data-symbol="common/filters;BodyParams;decorator;@;false;false;false;false"><a href="#/api/common/filters/bodyparams"class="symbol-container symbol-type-decorator symbol-name-commonfilters-BodyParams"title="BodyParams"><span class="symbol decorator"></span>BodyParams</a></li><li class="api-item" data-symbol="common/filters;Cookies;decorator;@;false;false;false;false"><a href="#/api/common/filters/cookies"class="symbol-container symbol-type-decorator symbol-name-commonfilters-Cookies"title="Cookies"><span class="symbol decorator"></span>Cookies</a></li><li class="api-item" data-symbol="common/filters;CookiesParams;decorator;@;false;false;false;false"><a href="#/api/common/filters/cookiesparams"class="symbol-container symbol-type-decorator symbol-name-commonfilters-CookiesParams"title="CookiesParams"><span class="symbol decorator"></span>CookiesParams</a></li><li class="api-item" data-symbol="common/filters;PathParams;decorator;@;false;false;false;false"><a href="#/api/common/filters/pathparams"class="symbol-container symbol-type-decorator symbol-name-commonfilters-PathParams"title="PathParams"><span class="symbol decorator"></span>PathParams</a></li><li class="api-item" data-symbol="common/filters;QueryParams;decorator;@;false;false;false;false"><a href="#/api/common/filters/queryparams"class="symbol-container symbol-type-decorator symbol-name-commonfilters-QueryParams"title="QueryParams"><span class="symbol decorator"></span>QueryParams</a></li><li class="api-item" data-symbol="common/filters;Session;decorator;@;false;false;false;false"><a href="#/api/common/filters/session"class="symbol-container symbol-type-decorator symbol-name-commonfilters-Session"title="Session"><span class="symbol decorator"></span>Session</a></li></ul>

## Usage

Models can be used at the controller level.
Here is our model:

```typescript
import  {Property, Minimum, PropertyType} from "@tsed/common";
import  {Description} from "@tsed/swagger";

class Person {
    @Property()
    firstName: string;
    
    @Property()
    lastName: string;
    
    @Description("Age in years")
    @Minimum(0)
    age: number;
    
    @PropertyType(String)
    skills: Array<string>;
}
```

> Note: `@PropertyType` allow to specify the type of a collection.

And its uses on a controller:

```typescript
import {Post, Controller, BodyParams} from "@tsed/common";
import {Person} from "../models/Person";

@Controller("/")
export class PersonsCtrl {

     @Post("/")
     save(@BodyParams() person: Person): Person {
          console.log(person instanceof Person); // true
          return person; // will be serialized according to your annotation on Person class.
     } 

     //OR
     @Post("/")
     save(@BodyParams('person') person: Person): Person {
          console.log(person instanceof Person); // true
          return person; // will be serialized according to your annotation on Person class.
     }
}
```
> In this example, Person model is used both as input and output types.

## Sérialisation

When you use a class model as a return parameter, the Converters service will use the JSON Schema
of the class to serialize the JSON object.

Here is an example of a model whose fields are not voluntarily annotated:
```typescript
class User {
    _id: string;
    
    @Property()
    firstName: string;
    
    @Property()
    lastName: string;
    
    password: string;
}
```

And our controller:

```typescript
import {Post, Controller, BodyParams} from "@tsed/common";
import {Person} from "../models/Person";

@Controller("/")
export class UsersCtrl {

    @Get("/")
    get(): User {
        const user = new User();
        user._id = "12345";
        user.firstName = "John";
        user.lastName = "Doe";
        user.password = "secretpassword";
          return 
    }
}
```

Our serialized `User` object will be:

```json
{
  "firstName": "John",
  "lastName": "Doe"
}
```
> Non-annotated fields will not be copied into the final object.

You can also explicitly tell the Converters service that the field should not be serialized with the decorator `@IgnoreProperty`.

```typescript
class User {
    @NotSerialize()
    _id: string;
    
    @Property()
    firstName: string;
    
    @Property()
    lastName: string;
    
    @IgnoreProperty()
    password: string;
}
```

## Type converters

The Converters service relies on a subservice set to convert the following types:

- Basics: [String, Number et Boolean](https://github.com/Romakita/ts-express-decorators/blob/master/src/common/converters/components/PrimitiveConverter.ts),
- Objects: [Date](https://github.com/Romakita/ts-express-decorators/blob/master/src/common/converters/components/DateConverter.ts) et [Symbol](https://github.com/Romakita/ts-express-decorators/blob/master/src/common/converters/components/SymbolConverter.ts),
- Collections: [Array](https://github.com/Romakita/ts-express-decorators/blob/master/src/common/converters/components/ArrayConverter.ts), [Map](https://github.com/Romakita/ts-express-decorators/blob/master/src/common/converters/components/MapConverter.ts) et [Set](https://github.com/Romakita/ts-express-decorators/blob/master/src/common/converters/components/SetConverter.ts).

> Set and Map types will be converted into an JSON object (instead of Array).

<ul class="api-list"><li class="api-item" data-symbol="common/converters;ArrayConverter;class;C;false;false;false;true"><a href="#/api/common/converters/arrayconverter"class="symbol-container symbol-type-class symbol-name-commonconverters-ArrayConverter"title="ArrayConverter"><span class="symbol class"></span>ArrayConverter</a></li><li class="api-item" data-symbol="common/converters;DateConverter;class;C;false;false;false;true"><a href="#/api/common/converters/dateconverter"class="symbol-container symbol-type-class symbol-name-commonconverters-DateConverter"title="DateConverter"><span class="symbol class"></span>DateConverter</a></li><li class="api-item" data-symbol="common/converters;MapConverter;class;C;false;false;false;true"><a href="#/api/common/converters/mapconverter"class="symbol-container symbol-type-class symbol-name-commonconverters-MapConverter"title="MapConverter"><span class="symbol class"></span>MapConverter</a></li><li class="api-item" data-symbol="common/converters;PrimitiveConverter;class;C;false;false;false;true"><a href="#/api/common/converters/primitiveconverter"class="symbol-container symbol-type-class symbol-name-commonconverters-PrimitiveConverter"title="PrimitiveConverter"><span class="symbol class"></span>PrimitiveConverter</a></li><li class="api-item" data-symbol="common/converters;SetConverter;class;C;false;false;false;true"><a href="#/api/common/converters/setconverter"class="symbol-container symbol-type-class symbol-name-commonconverters-SetConverter"title="SetConverter"><span class="symbol class"></span>SetConverter</a></li><li class="api-item" data-symbol="common/converters;SymbolConverter;class;C;false;false;false;true"><a href="#/api/common/converters/symbolconverter"class="symbol-container symbol-type-class symbol-name-commonconverters-SymbolConverter"title="SymbolConverter"><span class="symbol class"></span>SymbolConverter</a></li></ul>

### Example

Here an example of a type converter:

```typescript
import {IConverter, Converter} from "@tsed/common";

@Converter(String, Number, Boolean)
export class PrimitiveConverter implements IConverter {

    deserialize(data: string, target: any): String | Number | Boolean | void {

        switch (target) {
            case String:
                return "" + data;

            case Number:
                const n = +data;
                return n;

            case Boolean:

                if (data === "true") return true;
                if (data === "false") return false;

                return !!data;
        }

    }

    serialize(object: String | Number | Boolean): any {
        return object;
    }
}
```

### Create a custom converter

Ts.ED creates its own converter in the same way as the previous example.

To begin, you must add to your configuration the directory where are stored
your classes dedicated to converting types.

 
```typescript
import {ServerLoader, ServerSettings} from "@tsed/common";
import Path = require("path");
const rootDir = Path.resolve(__dirname);

@ServerSettings({
   componentsScan: [
       `${rootDir}/converters/**/**.js`
   ]
})
export class Server extends ServerLoader {
   
}       
```

Then you will need to declare your class with the `@Converter` annotation:


```typescript
import {ConverterService, Converter, IConverter, IDeserializer, ISerializer} from "@tsed/common";

@Converter(Array)
export class ArrayConverter implements IConverter {

    deserialize<T>(data: any[], target: any, baseType: T, deserializer: IDeserializer): T[] {
         
        if (isArrayOrArrayClass(data)) {
            return (data as Array<any>).map(item =>
                deserializer(item, baseType)
            );
        }

        return [data];
    }

    serialize(data: any[], serializer: ISerializer) {
        return (data as Array<any>).map(item =>
            serializer(item)
        );
    }
}
```

?> Note that this example will replace the default Ts.ED converter.

It is therefore quite possible to replace all converters with your own classes (especially the Date).

## Validation

The Converter service provides some of the validation of a class model.
It will check the consistency of the JSON object with the data model. For example :

- If the JSON object contains one more field than expected in the model (`validationModelStrict` or `@ModelStrict`).
- If the field is mandatory `@Required`,
- If the field is mandatory but can be `null` (`@Allow(null)`).

Here is a complete example of a model:


```typescript
class EventModel {
    @Required()
    name: string;
     
    @PropertyName('startDate')
    startDate: Date;

    @Property({name: 'end-date'})
    endDate: Date;

    @PropertyType(TaskModel)
    @Required()
    @Allow(null)
    tasks: TaskModel[];
}

class TaskModel {
    @Required()
    subject: string;
    
    @Property()
    rate: number;
}
```

### validationModelStrict

The `strict` validation of an object can be modified either globally or for a specific model.

Here is an example of `strict` validation:


```typescript
import {InjectorService, ConvertersService, Required, Property} from "@tsed/common";

InjectorService.load();

class TaskModel {
    @Required()
    subject: string;
    
    @Property()
    rate: number;
}

const convertersService = InjectorService.get(ConvertersService);
convertersService.validationModelStrict = true;

convertersService.deserialize({unknowProperty: "test"}, TaskModel); // BadRequest
```

#### Global

```typescript
import {ServerLoader, ServerSettings} from "@tsed/common";

@ServerSettings({
   validationModelStrict: true | false
})
export class Server extends ServerLoader {
   
}      
```
> By default, the Converters service is configured on the `strict` mode.

#### ModelStrict

```typescript
import {ConvertersService, ModelStrict, Required, Property} from "@tsed/common";

@ModelStrict(false)
class TaskModel {
   @Required()
   subject: string;
   
   @Property()
   rate: number;
   [key: string]: any; // recommended
}
````

In this case, the service will not raise more exception:

```typescript
import {InjectorService, ConvertersService, ModelStrict, Required, Property} from "@tsed/common";

InjectorService.load();

const convertersService = InjectorService.get(ConvertersService);
convertersService.validationModelStrict = true;

const result = convertersService.deserialize({unknowProperty: "test"}, TaskModel);
console.log(result) // TaskModel {unknowProperty: "test"}
```

?> If you have disabled `strict` validation at the global level, you can use the `@ModelStrict(true)` decorator
 to enable validation for a specific model.