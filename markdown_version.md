
# Visualising data on map in Python


```python
import matplotlib.pyplot as plt
import matplotlib.cm 
%matplotlib inline

from mpl_toolkits.basemap import Basemap
from matplotlib.patches import Polygon
from matplotlib.collections import PatchCollection
from matplotlib.colors import Normalize
```

Now create and draw a figure.  Instantiate the map object.  The arguments are as follows:
- first two are clear
- `lat_0`,`lon_0` are the lat and long of the centre point
- `llcrnrlon` is lower left corner lon and the others are similar.


```python
fig, ax = plt.subplots(figsize=(10,20))
m = Basemap(resolution='c',
           projection='merc', 
           lat_0=54.5,
           lon_0=-4.36,
           llcrnrlon=-6, llcrnrlat = 49.5, urcrnrlon = 2, urcrnrlat=55.2)
```


![png](Map%20visualistaion_files/Map%20visualistaion_3_0.png)



```python
m.drawmapboundary(fill_color='#46bcec')
m.fillcontinents(color='#f2f2f2', lake_color='46bcec')
m.drawcoastlines()
```

    /Users/charliedickens/anaconda3/lib/python3.6/site-packages/mpl_toolkits/basemap/__init__.py:1698: MatplotlibDeprecationWarning: The axesPatch function was deprecated in version 2.1. Use Axes.patch instead.
      limb = ax.axesPatch
    /Users/charliedickens/anaconda3/lib/python3.6/site-packages/mpl_toolkits/basemap/__init__.py:1767: MatplotlibDeprecationWarning: The get_axis_bgcolor function was deprecated in version 2.0. Use get_facecolor instead.
      axisbgc = ax.get_axis_bgcolor()





    <matplotlib.collections.LineCollection at 0x116794518>




![png](Map%20visualistaion_files/Map%20visualistaion_4_2.png)

