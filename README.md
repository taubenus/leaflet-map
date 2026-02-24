A leaflet html file that can be embedded via `<iframe>` in LogSeq to generate an Open Street Maps map view centered on markers specified in the iframe.

Add a macro to `config.edn`
``` 
:macros {
         :location "
       <div> <iframe src='https://taubenus.github.io/leaflet-map/leaflet-map.html?markers=$1&zoom=16' 
         width='100%' 
         height='640' 
         style='border:0; border-radius:8px; overflow:hidden;' 
         ></iframe> </div>"
         }
```

call Macro in LogSeq: `{{location <lat_1>;<lon_1>|...|<lat_n>;<lon_n>}}`
