# Datos del geoportal del Proyecto Cosecha de Agua
Datos curados y transformados para el portal

Ríos
```shell
ogr2ogr -f GeoJSON -nln rios-seg -t_srs EPSG:4326 -makevalid geo/rios/rios-seg.geojson ../datos-originales/geo/rios/rios_seg.shp
```
