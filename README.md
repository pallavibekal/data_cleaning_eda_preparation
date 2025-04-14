# data_cleaning_eda_preparation

Program: Averaging large THEMIS Inertia maps


Convert an image file (MELLON TI Map) into numpy file and store
"The thermal inertia of Mars is a physical property that controls the diurnal and seasonal cycles in surface temperature. It is defined as a function of the thermal conductivity, heat capacity, and density, all of which depend primarily on the physical structure of the surface layer. As such, thermal inertia provides information about the nature of the surface of Mars and the types of materials from which it is composed. Interpreting thermal inertia can be complicated by the variety of structures and material properties that result in the same thermal inertia value. In general, variations in the thermal conductivity have the greatest influence on the thermal inertia. Factors such as soil grain size, cementing or induration, rock abundance, the presence of bedrock, and surface heterogeneity all play an important role." - https://www.cambridge.org/core/books/martian-surface/thermal-inertia-of-the-surface-of-mars/683F86021F4BB3790DD78C4C2513DF45

EMM gives us Surface Temperature over large areas that allows us to study the thermal inertia variations across MARS over different Solar Longitudes. Before we develop this data product, we need to compare the thermal inertia obtained via EMM with multiple other missions. We use the Mellon Maps created using TES Bolometric Data, and THEMIS thermal inertia maps.

In this program we read the Mellon Maps using the pdr library developed by NASA. The size of the file is 3600 X 7200. We average 1x1 degree Lat Lon and store as a numpy file for other programs in the pipeline to process and use.

Data Format: Image (Read using the PDR library from NASA)

https://se.psi.edu/inertia/2007/

image.png


