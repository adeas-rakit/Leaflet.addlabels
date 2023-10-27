## Leaflet.addlabels
A Leaflet plugin for showing labels along polylines.

### Usage

``` js
// Create a new renderer as follows (use any options as necessary):
var addLabelsRenderer = new L.AddLabels({
      collisionFlg : true,
      propertyName : 'name',
      showLabelIf: function(layer) {
        return true; //layer.properties.type == "primary";
      },
      fontStyle: {
        dynamicFontSize: false,
        fontSize: 10,
        fontSizeUnit: "px",
        lineWidth: 4.0,
        fillStyle: "black",
        strokeStyle: "white",
      },
    })

// Create a new map and attach the renderer created above:
var map = new L.Map('map', {
    renderer : addLabelsRenderer, //Custom Canvas Renderer
});
```
### Building

    npm install && npm run build

### Supported Leaflet Versions

Leaflet 1.0 and later versions should be supported. Earlier versions probably won\'t work (not even tested anymore).

---