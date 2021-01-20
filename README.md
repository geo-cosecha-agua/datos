# Datos del geoportal del Proyecto Cosecha de Agua
Datos curados y transformados para el portal

Ríos
```shell
ogr2ogr -nln rios-seg-temp -s_srs EPSG:32616 -t_srs EPSG:4326 -makevalid geo/rios/rios-seg-temp.geojson ../datos-originales/geo/rios/rios_seg.shp
ogr2ogr -nln rios-seg -s_srs EPSG:4326 -t_srs EPSG:4326 -makevalid -clipsrc geo/municipios/municipios-disuelto.geojson geo/rios/rios-seg.geojson geo/rios/rios-seg-temp.geojson
del geo\rios\rios-seg-temp.geojson
```

Microcuencas
```shell
ogr2ogr -nln microcuencas-temp -s_srs EPSG:32616 -t_srs EPSG:4326 -makevalid geo/microcuencas/microcuencas-temp.geojson ../datos-originales/geo/microcuencas/microseg.shp
ogr2ogr -nln microcuencas -s_srs EPSG:4326 -t_srs EPSG:4326 -makevalid -clipsrc geo/municipios/municipios-disuelto.geojson geo/microcuencas/microcuencas.geojson geo/microcuencas/microcuencas-temp.geojson
del geo\microcuencas\microcuencas-temp.geojson
```

Suelos
```shell
ogr2ogr -nln suelos-temp -s_srs EPSG:32616 -t_srs EPSG:4326 -makevalid geo/suelos/suelos-temp.geojson ../datos-originales/geo/suelos/ordenes_identidad.shp
ogr2ogr -nln suelos -s_srs EPSG:4326 -t_srs EPSG:4326 -makevalid -clipsrc geo/municipios/municipios-disuelto.geojson geo/suelos/suelos.geojson geo/suelos/suelos-temp.geojson
del geo\suelos\suelos-temp.geojson
```
