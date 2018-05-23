# AutoHex
Create hexmaps from geoJSON boundary files using an energy minimisation technique.

## How it works
1. Load a GeoJSON file and find the centroid of each polygon (we use Leaflet to help with).
2. Create a grid of hexes, and place the collection of centroids on top of it.
3. In turn, the nearest unassigned hex to each centroid is highlighted. An "energy cost" is calculated which penalises the distance between each centroid and its corresponding hex.
4. Slightly reduce the scale of the collection of centroids and repeat step 3.
5. Repeat until the scale is tiny and then select the zoom at which.
6. We use Raphael.js to visualise all of this.
