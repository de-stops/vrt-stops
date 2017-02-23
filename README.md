# vrt-stops

This is a simple script to download all [VRT](http://www.vrt-info.de/) stops as [GTFS-compatible CSV](https://developers.google.com/transit/gtfs/reference/stops-file).

The script uses the following endpoint:

```
http://efa9.vrn.de/vrt_mobile/XML_COORD_REQUEST?mId=efa_www&language=en&itdLPxx_mapName=MRCV&coordOutputFormat=WGS84%5BGGZHTXX%5D&boundingBox=1&boundingBoxLU={minx}%3A{miny}%3AWGS84%5BDD.DDDDD%5D&boundingBoxRL={maxx}%3A{maxy}%3AWGS84%5BDD.DDDDD%5D&inclFilter=1&purpose=5&max=-1&coordListFormat=STRING&itdLPxx_mdvMapName=mdvMap_efaFullPanelMap&coordListOutputFormat=STRING&scale=13&outputFormat=JSON&type_1=STOP&inclDrawClasses_1=
```

It starts from bounding box `(5, 47, 15, 56)` and works down to smaller quadrants.

The script produces CSV output in the following format:

```
"stop_id","stop_name","stop_lon","stop_lat","stop_code"
"17020001","Affler, Ort",6.1531362216000005,50.01468712570001,"de:7232:20001"
```

# Usage

```
npm install
node index.js
```

# Disclaimer

Usage of this script may or may not be legal, use on your own risk.  
This repository provides only source code, no data.

# License

Source code is licensed under [BSD 2-clause license](LICENSE). No license and no guarantees implied on the produced data, produce and use on your own risk.