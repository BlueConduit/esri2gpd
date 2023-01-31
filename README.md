# esri2gpd (the BluesConduit Remix)


A lightweight Python tool to scrape features from the ArcGIS Server REST API and return a geopandas GeoDataFrame
python.

Inspired by the R package [esri2sf](https://github.com/yonghah/esri2sf/).

## Installation


```
python -m pip install git+https://github.com/BlueConduit/esri2gpd.git
```


## Example

```python
In [1]: import esri2gpd

In [2]: gdf = get("https://cityworks.toledo.oh.gov/arcgis443/rest/services/Cityworks/WaterOperational/MapServer/30", max_record_count=5000)
/Users/nicholasshea/blueconduit/service-line-pipeline/esri2gpd/esri2gpd/core.py:94: UserWarning: Long download time — total download will require 23 separate requests
  warnings.warn(

In [3]: gdf
Out[3]: 
                                                 geometry  OBJECTID    AssetID  ... DateLeadReplaced  DateCustSideReplaced Date_Material_Verified
0       LINESTRING (-83.60065 41.60391, -83.60033 41.6...         1  WSL101077  ...              NaN                   NaN                    NaN
1       LINESTRING (-83.60135 41.72673, -83.60134 41.7...         2  WSL103021  ...              NaN                   NaN                    NaN
2       LINESTRING (-83.55148 41.67306, -83.55148 41.6...         4  WSL106476  ...              NaN                   NaN                    NaN
3       LINESTRING (-83.52278 41.63360, -83.52287 41.6...         5  WSL107470  ...              NaN                   NaN                    NaN
4       LINESTRING (-83.52484 41.68571, -83.52484 41.6...         6  WSL108884  ...              NaN                   NaN                    NaN
...                                                   ...       ...        ...  ...              ...                   ...                    ...
115417  LINESTRING (-83.62359 41.65001, -83.62361 41.6...    348830  WSL624850  ...  1674742899000.0                   NaN                   None
115418  LINESTRING (-83.48747 41.65996, -83.48748 41.6...    348831  WSL624851  ...              NaN                   NaN                   None
115419  LINESTRING (-83.46834 41.72188, -83.46833 41.7...    348832  WSL624852  ...              NaN                   NaN                   None
115420  LINESTRING (-83.51475 41.63287, -83.51474 41.6...    349154  WSL624853  ...              NaN                   NaN                   None
115421  LINESTRING (-83.51571 41.63962, -83.51570 41.6...    349155  WSL624854  ...              NaN                   NaN                   None

[115422 rows x 40 columns]

```
