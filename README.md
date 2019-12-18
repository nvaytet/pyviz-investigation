[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/nvaytet/pyviz-investigation/master)

# pyviz-investigation

## Investigation of the python data visualization landscape

We explored the Python data visualization ecosystem by selecting the most commonly used open-source libraries and testing them in a set of 10 standard [use cases](examples/matplotlib.ipynb). The packages were evaluated on their richness of features, capabilities for interaction (primarily in a Jupyter notebook environment), project sustainability, documentation, and performance.

Our findings are best represented as a ranked list:

1. [`matplotlib (+ipyvolume)`](report.ipynb#matplotlib): `matplotlib` is the most mature and well-established project, with the largest community/user base, and great case coverage. Interaction with Jupyter widgets works well. However, 3D performance is poor, and it should be coupled to a 3D-specific library (we found `ipyvolume` to be a very good candidate).


2. [`plotly`](report.ipynb#plotly): best use case coverage (including 3D), excellent interactivity, great performance, has a `Dash` platform for creating in-browser apps. It could benefit from some `Datashader`-like functionality for large datasets. Performance is however poor when back-and-forth communication is required between the plot and the Jupyter Kernel, as is the case for slider widgets, for example.


3. [`HoloViz`](report.ipynb#holoviz): very similar to `plotly` in case coverage, very high performance (especially via the `Datashader` method), makes interactions much easier to implement than `bokeh`, also has a `Panels` utility for apps, but is a young project that still feels scattered over different sub-projects, not as unified as `plotly`.


4. [`bokeh`](report.ipynb#bokeh): good case coverage, many interactions possibilities, but lacking 3D visualization, and interactions with buttons/sliders must be implemented in javascript.


5. [`pyqtgraph`](report.ipynb#pyqtgraph): outstanding performance, 1 to 3D under a unified interface, wide range of interactions, but only one developer, project feels un-finished (especially 3D graphs), and integration in Jupyter notebooks is poor.


6. [`bqplot`](report.ipynb#bqplot): focuses on interactions (every item in a plot is a clickable/draggable widget), the diversity of which, unfortunately, never makes up for the sad performance. It would be worth re-visiting this young project in a year's time.
