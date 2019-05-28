# s-p_from_fdsn
Using FDSN event service, get and visualize S-P data

# Purpose
Given the location scatter for earthquakes near volcanoes, the volcano monitoring team sometimes wonder about how S-P interval might be used to see if any hypocentral 'migration' can be seen. In an ideal situation the quality of 'routine monitoring locations' would be sufficient to provide the necessary data, but at the moment it is not.

# Detail
Previous efforts to look at changes in S-P at volcanoes, such as Raoul Island in 2006, relied on manually picking P- and S-phases. In my view, manual picking is not the best use of my time. An easy to implement alternative is to use picks routinely made using earthquake location with SC3. Picks are extracted from GeoNet using ObsPy's FDSN_Client and the client.get_events function.

While the code used to iterate through the various phase picks is clunky, and I'm sure there is a nicer alternative, only I don't know what, its based of one of GeoNet's data tutorials https://github.com/GeoNet/data-tutorials/blob/master/Seismic_Data/Python/GeoNet_FDSN_demo_event.ipynb, so its a good first choice.

# Output and Visualization
- A summary of the number of phases, including P-phases for the sites chosen, and S-P intervals for those sites.
- A time-series of S-P versus earthquake origin time
![GitHub Logo](/readme_images/white_island_s-p_scatter.png)
- A boxpot showing the distribution of S-P intervals for the sites chosen
![GitHub Logo](/readme_images/white_island_s-p_boxplot.png)

# Maturity
This is not a mature product.
