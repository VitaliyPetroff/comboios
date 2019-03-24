# `trip(id)`

Get all stopovers for a trip id obtained using the [journeys](./journeys.md) or [stopovers](./stopovers.md) method. Returns a [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/promise) that will resolve in a trip object.

```js
const comboios = require('comboios')

comboios.trip('3400@2019-05-09')
.then(console.log)
.catch(console.error)
```

## Response

```js
{
    "id": "3400@2019-05-09",
    "line": {
        "type": "line",
        "id": "3400",
        "name": "3400",
        "product": "Regional",
        "productCode": "R",
        "mode": "train",
        "public": true,
        "operator": {
            "type": "operator",
            "id": "cp",
            "name": "Comboios de Portugal",
            "url": "https://www.cp.pt/"
        }
    },
    "stopovers": [
        {
            "type": "stopover",
            "stop": {
                "type": "station",
                "id": "94-2006",
                "name": "Porto - Campanha"
            },
            "arrival": "2019-05-08T23:00:00.000Z",
            "arrivalPlatform": null,
            "departure": "2019-05-08T23:55:00.000Z",
            "departurePlatform": null
        },
        {
            "type": "stopover",
            "stop": {
                "type": "station",
                "id": "94-39172",
                "name": "General Torres"
            },
            "arrival": "2019-05-08T23:58:00.000Z",
            "arrivalPlatform": null,
            "departure": "2019-05-08T23:59:00.000Z",
            "departurePlatform": null
        },
        // …
        {
            "type": "stopover",
            "stop": {
                "type": "station",
                "id": "94-30007",
                "name": "Lisboa - Santa Apolonia"
            },
            "arrival": "2019-05-09T04:59:00.000Z",
            "arrivalPlatform": null,
            "departure": "2019-05-09T23:00:00.000Z",
            "departurePlatform": null
        }
    ]
}
```
