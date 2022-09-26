# Services

Godzilla Form parser provides two types of services that you can use with your forms `GodzillaDataService`
and `GodzillaValidatorService`, both of them are based on `GodzillaService` which can be imported from `godzilla-core`
library.

## GodzillaDataService

This Service is mainly used to update the form input data from any service. For example, if you want to use a `DropDown`
list and the data for this input you want to be a dynamic from any service instead of static values.

### How to use it?

#### Create GodzillaDataService

First, you need to create a new service class implemented from `GodzillaDataService`.

```typescript
@Injectable()
export class MyDataDataService implements GodzillaDataService {

  constructor(private http: HttpClient) {
  }

  async getData(): Promise<GodzillaFormCombinedValues[]> {
    return await firstValueFrom(this.http.get<GodzillaFormCombinedValues[]>("https://domain.com/service"))
  }
}

```

`getData()` only accept `GodzillaFormCombinedValues[]` but you can map any response type like below

```typescript
 async
getData()
:
Promise < GodzillaFormCombinedValues[] > {
  let httpRequest = this.http.get<GodzillaFormCombinedValues[]>("https://domain.com/service")
    .pipe(
      map(o =>
        o.map((item: MyInterface): GodzillaFormCombinedValues => ({
          label: item.label,
          value: item.value
        }))));
  return await firstValueFrom(httpRequest)
}
```

#### Module provider

On your module you can provide as many as `GodzillaDataService` you like below:

```typescript
  providers: [{
  provide: GODZILLA_OPTIONS,
  useValue: <GodzillaOptions>{
    dataServices: {
      myService: {provide: MyDataDataService},
      mySecondService: {provide: MySecondDataDataService},
    }
  }
}]

```

`myService` is service reference, this reference need to be used later with Godzilla Builder.

#### Godzilla Builder & GodzillaDataService

If you drag and drop any list form element like `DropDown` or `RadioGroups` and then go to the element setting under the
In General configuration, you will see a new option called `Values Source`; change it to `Service` and then type the service
reference in `Values service name` field.

## GodzillaValidatorService

**TODO**
