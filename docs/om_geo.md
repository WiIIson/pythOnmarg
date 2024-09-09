# `om_geo` Documentation

## Description

Retrieves a selected year of data from the Ontario Marginalization Index aggregated by a given level and joins it with geographic data from Stats Canada.

```python
om_geo(year, level)
```

## Parameters

`year`: int
- Year of data to pull from. Must be one of "2011", "2016", or "2021".

`level`: str
- Geographic level data is aggregated to. Must be one of "DAUID", "CTUID", "CSDUID", "CCSUID", "CDUID", "CMAUID", "PHUUID", "LHINUID", or "LHIN_SRUID".

## Exceptions

Raises an exception if there are no records for the provided year or level.

## Returns

`om_geo`: gpd.GeoDataFrame
- Returns a geodataframe of the requested data.

## Example

```python
gdf = om_geo(2021, "DAUID")
```