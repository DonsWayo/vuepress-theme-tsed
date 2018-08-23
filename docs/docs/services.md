# Services

The decorator `@Service()` declare a new service can be injected in other service or controller on there `constructor()`.
All services annotated with `@Service()` are constructed one time.

## Configuration

You must adding the `services` folder on `componentsScan` attribute in your server settings as follow :
 
```typescript
import {ServerLoader} from "@tsed/common";

@ServerSettings({
   rootDir,
   mount: {
      '/rest': `./controllers/**/**.js`
   },
   componentsScan: [
       `./services/**/**.js`
   ],
   customServiceOptions: {}
})
export class Server extends ServerLoader {
   
}       
```

## Decorators

<ul class="api-list"><li class="api-item" data-symbol="common/di;Inject;decorator;@;false;false;false;false"><a href="#/api/common/di/inject"class="symbol-container symbol-type-decorator symbol-name-commondi-Inject"title="Inject"><span class="symbol decorator"></span>Inject</a></li><li class="api-item" data-symbol="common/di;OverrideProvider;decorator;@;false;false;false;false"><a href="#/api/common/di/overrideprovider"class="symbol-container symbol-type-decorator symbol-name-commondi-OverrideProvider"title="OverrideProvider"><span class="symbol decorator"></span>OverrideProvider</a></li><li class="api-item" data-symbol="common/di;OverrideService;decorator;@;false;false;false;false"><a href="#/api/common/di/overrideservice"class="symbol-container symbol-type-decorator symbol-name-commondi-OverrideService"title="OverrideService"><span class="symbol decorator"></span>OverrideService</a></li><li class="api-item" data-symbol="common/di;Service;decorator;@;false;false;false;false"><a href="#/api/common/di/service"class="symbol-container symbol-type-decorator symbol-name-commondi-Service"title="Service"><span class="symbol decorator"></span>Service</a></li></ul>

## Declaring a service

Create a new file in your services folder. Create a new Class definition and add the `@Service()` annotation on your class.

```typescript
@Service()
export class MyService implements OnInit, BeforeRoutesInit, OnRoutesInit, AfterRoutesInit, OnServerReady {
    private settings = {};
    
    constructor(
        private serverSettings: ServerSettingsService
    ) {
        this.settings = this.serverSettings.get('customServiceOptions');
    }
    
    public getSettings() {
        return this.settings;
    }
}
```

Finally, inject the service to another service:
```typescript
import {MyService} from "./MyService";

@Service()
export class FooService {
    constructor(private myService: myService) {
    
    }
}
```
Or to another controller: 

```typescript
import {MyService} from "./MyService";

@Controller('/rest') 
class MyController {
    constructor(private myService: MyService){
    
    }
}  
```

## Override a Service

The decorator [@OverrideService](/api/common/di/overrideservice.md) gives you the ability to
override some internal Ts.ED service like the [ParseService](/api/common/filters/parseservice.md).

Example usage:
```typescript
import {OverrideService, ParseService} from "@tsed/common"

@OverrideService(ParseService)
class CustomParseService extends ParseService {
    
}
```

## Lifecycle Hooks

Ts.ED 2.x introduce a new Lifecycle Hooks on the service that follows the [Lifecycle of the ServerLoader](docs/server-loader/lifecycle-hooks.md).
This lifecycle hooks that provide visibility into these key life moments and the ability to act when they occur.


A service that uses one of the phases of the lifecycle can add a number of things and can be completely autonomous.
This is the case with the example of the socket server (See the section [How to integrate Socket.io](tutorials/socket-io.md)).

This schemes resume the order of the service's lifecycle along the ServerLoader's lifecycle.

![lifecycle-hooks](./../assets/hooks-in-sequence.png)

Each interface has a single hook method whose name is the interface name prefixed with `$`. For example, the `OnInit`
interface has a hook method named `$onInit()` (old name `$onInjectorReady`) or that Ts.ED calls when all services are built.

```typescript
@Service()
export class MyService implements OnInit, BeforeRoutesInit, OnRoutesInit, AfterRoutesInit, OnServerReady {
    private settings = {};

    constructor(
        private serverSettings: ServerSettingsService
    ) {
        this.settings = this.serverSettings.get('customServiceOptions');
    }

    $onInit(): Promise<any> | void {
        console.log('All services is ready');
    }

    $beforeRoutesInit(): Promise<any> | void {
        console.log('Controllers and routes isn\'t mounted');
    }

    $onRoutesInit(components: IComponentScanned[]): Promise<any> | void {
       console.log('Controllers and routes are being built');

    }

    $afterRoutesInit(): Promise<any> | void {
        console.log('Controllers and routes are built');
    }

    $onServerReady(): Promise<any> | void {
        console.log('Server is ready and listen the port');
    }
}
```

Hook | Purpose and Timing
---|---
$onInit | Respond after Injector have initialized all Services in the registry.
$beforeRoutesInit | Respond before loading the controllers. The middlewares and filters are already built.
$onRoutesInit | Launch the build of the controllers. This hook provide a list of component scanned by componentsScan.
$afterRoutesInit | Respond after the controllers build.
$onServerReady | Respond when the server is ready. At this step, HttpServer or/and HttpsServer object is available. The server listen the port.


::: tip Interfaces are optional

The interfaces are optional for JavaScript and Typescript developers from a purely technical perspective.
The JavaScript language doesn't have interfaces. Ts.ED can't see TypeScript interfaces at runtime because they disappear from the transpiled JavaScript.

Nonetheless, it's good practice to add interfaces to TypeScript directive classes in order to benefit from strong typing and editor tooling.
:::