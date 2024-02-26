[<- Trở về](../README.md#map-tiles)
<div align="center">
  <br/>
  <img alt="logo" height="200" src="https://developers.google.com/static/maps/images/maps-icon.svg"/>
  <h1>Google Map Tiles</h1> 
</div>

### Url
http://{[subdomains](#subdomains)}.google.com/vt/lyrs={[mapTypes](#map-types)},{[layer](#map-layer-có-thể-chọn-nhiều-layer)}&hl={[lang](#map-language)}&apistyle={[apistyle](#a)}&x={x}&y={y}&z={z}

### Subdomains: 
    mt0, mt1, mt2, mt3, mts0, mts1, mts2, mts3

### Map types:
    - h = roads only
    - m = standard roadmap
    - p = terrain
    - r = somehow altered roadmap
    - s = satellite only
    - t = terrain only
    - y = hybrid

### Map Layer (có thể chọn nhiều layer)
    - traffic = Traffic layer
    - transit = Transit layer
    - bike = Bike layer

### Map Language ([IETF subtags](https://en.wikipedia.org/wiki/IETF_language_tag#List_of_common_primary_language_subtags))
    - vi = Tiếng Việt
    - en = English
    - ...

### ApiStyle (tạo style ở [đây](https://mapstyle.withgoogle.com/) tham khảo gen json sang string ở [đây](https://github.com/julienben/gmaps-apistyle-encoder/tree/master))
#### FeatureTypes: s.t
    - 0 = all
    - 1 = administrative
    - 17 = administrative.country
    - 21 = administrative.land_parcel
    - 19 = administrative.locality
    - 20 = administrative.neighborhood
    - 18 = administrative.province
    - 5 = landscape
    - 81 = landscape.man_made
    - 82 = landscape.natural
    - 2 = poi
    - 37 = poi.attraction
    - 33 = poi.business
    - 34 = poi.government
    - 36 = poi.medical
    - 40 = poi.park
    - 38 = poi.place_of_worship
    - 35 = poi.school
    - 39 = poi.sports_complex
    - 3 = road
    - 50 = road.arterial
    - 49 = road.highway
    - 51 = road.local
    - 4 = transit
    - 65 = transit.line
    - 66 = transit.station
    - 6 = water
#### ElementType: s.e
    - g = geometry
    - g.f = geometry.fill
    - g.s = geometry.stroke
    - l = labels
    - l.i = labels.icon
    - l.t = labels.text
    - l.t.f = labels.text.fill
    - l.t.s = labels.text.stroke
#### Styler:
    - p.c = color (RGBA hex-value #aarrggbb)
    - p.g = gamma (float between 0.01 and 10)
    - p.h = hue (RGB hex-value #rrggbb)
    - p.il = invert_lightness (true/false)
    - p.l = lightness (float between -100 and 100)
    - p.s = saturation (float between -100 and 100, ex: p.s:0)
    - p.v = visibility (on/simplified/off, ex: p.v:on)
    - p.w = weight
    - >=0 = integer
### Example
- https://mt0.google.com/vt/lyrs=m&hl=vi&x={x}&y={y}&z={z}
- https://mts2.google.com/vt/lyrs=y,traffic&hl=en&x={x}&y={y}&z={z}
- https://mts3.google.com/vt/lyrs=m,transit,bike&hl=vi&x={x}&y={y}&z={z}
- https://mts3.google.com/vt/lyrs=m,transit&hl=vi&apistyle=s.t:3|p.c:FFFFFFFF&x={x}&y={y}&z={z}

### Tài liệu tham khảo
- https://stackoverflow.com/questions/23017766/google-maps-tile-url-for-hybrid-maptype-tiles 
- https://www.codeproject.com/Articles/14793/How-Google-Map-Works
- https://github.com/julienben/gmaps-apistyle-encoder/tree/master
- https://stackoverflow.com/questions/34311747/whats-the-url-to-download-map-tiles-from-google-maps 
- https://stackoverflow.com/questions/23457916/how-to-get-latitude-and-longitude-bounds-from-google-maps-x-y-and-zoom-parameter