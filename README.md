# MATLAB-cosmological-parameter-LSQ-fit
This code uses LSQ to fit a luminosity distance function to data from SCP with z&lt;0.8, as a part of a supervised research on the expansion of the universe.

# Research

    This research set out to describe a homogeneous and isotropic model of universe and its expansion rate.
    By compiling data from SCP (Supernova Cosmology Project) findings into a graph, where the x-axis is the supernova redshift 
    and the y-axis is it's luminosity distance, and using the LSQ method to find a best-fit luminosity distance for redshift function 
    that contained the parameters needed to describe this model of the universe for the graph, I was able find those paramters and 
    reach conclusions about the universe and its expansion rate.

# Definitions

  - H: Hubble parameter (km/s/mpc).
  - Omega_M: ratio of matter density to critical density.
  - Omega_Lambda: ratio of vaccum (dark) energy density to critical density.
  - Omega_R: ratio of relative particle energy density to critical density.
  - Omega_K: universe curvature parameter (persumed to be 0 in this research).
  - Omega_Lambda + Omega_R + Omega_M + Omega_K = 1

# Code

    This code defines an LSQ error function for the luminosity distance function.
    This code uses the built-in fminsearch function to find the minimum value for the LSQ error function.
    --- USE THE XLSX FILE FOR THE SUPERNOVA DATABASE AND CHANGE THE FILE LOCATION IN THE CODE ACCORDINGLY ---

### Algorithm

    Set starting values for the parameters randomly.
    Constrain the parameters for physically possible values (Relative particle energy density not greater than 0.1 and non negative)
    Find the closest minimum value point to those starting values.
    Store the parameter values that correspond to the minimum point.
    Repeat in a recursive manner 150 times.
    Create a mean average from the 150 results and calculate statistical error
    Plot the luminsoity distance function given the final results

# Deriving Basic Conclusions from the Results

  - Universe deacceleration parameter (q): q = Omega_M / 2 - Omega_Lambda.
  - Age of the universe: 1/H.

### This research was supervised by the Weizmann Institute of Science
