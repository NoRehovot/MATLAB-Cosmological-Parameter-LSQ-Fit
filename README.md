# MATLAB-cosmological-parameter-LSQ-fit
This project uses MATLAB in order to estimate the cosmological density and hubble parameters, as part of a research on the expansion of the universe in collaboration with the Weizmann Institute of Science.

# Research Project

    In this project I set out to describe a homogeneous and isotropic model of universe and its expansion rate.
    By compiling data from SCP (Supernova Cosmology Project) findings into a graph, where the x-axis is the supernova redshift 
    and the y-axis is it's luminosity distance, and using the LSQ method to find a best-fit luminosity distance for redshift function 
    that contained the parameters needed to describe this model of the universe for the graph, I was able find those paramters and 
    reach conclusions about the universe and its expansion rate.

# Definitions

  ### Redshift
    Redshift is a phenomenon related to the doppler effect that happens when light waves are stretched out, making them appear more 
    red than they would normally be. This stretching happens when an object that emits light, such as a star or a galaxy, is moving 
    away from us. The faster the object is moving away, the greater the stretching of the light waves and the more pronounced the 
    redshift.

    We use redshift to learn about the universe. By measuring how much an object's light has been redshifted, we can determine
    how quickly it's moving away from us and how far away it is.

  ### Luminosity Distance
    Luminosity distance is a measure of how bright an object appears to be from a distance. It takes into account not only the actual 
    brightness of the object but also how far away it is from us. The farther away an object is, the less bright it will appear, 
    even if it is actually very bright.

    Luminosity distance is also used in cosmological studies. By measuring how bright an object appears to be, we can calculate how 
    far away it is. 
  
  #### Both redshift and luminosity distance help us understand the size and structure of the universe, as well as how it's changing over time.
  
  ### Density Parameters of the Universe
    The density parameters of the universe refer to how much matter and energy there is in the universe compared to how much there 
    would need to be to achieve a certain outcome. There are five different density parameters that are commonly discussed: the 
    critical density, the matter density, the vacuum (dark) energy density, the raletivistic particle energy density and the curvature 
    parameter.

    The critical density is the amount of matter and energy needed for the universe to be flat - meaning that it would continue to 
    expand at the same rate forever. The matter density is the amount of regular matter, like stars and planets, in the universe. The 
    dark energy density is the amount of energy that is causing the universe's expansion to accelerate. The relativistic particle energy 
    is the amount of energy caused by relativistic particles. The curvature parameter describes the shape of the universe: 0 is for a 
    flat universe, 1 is for positive curvature and -1 is for negative curvature.

    If the matter density is higher than the critical density, the universe would eventually stop expanding and collapse back in on 
    itself. If the matter density is lower than the critical density, the universe would expand forever. If the dark energy density is 
    high enough, it could cause the universe to expand at an accelerating rate.
    
    We study the density parameters of the universe to understand its overall structure and evolution. By measuring the amount of matter 
    and energy in the universe, we can make predictions about its future and how it will change over time.
    
    Useful parameter definitions:
    - Omega: ratio of average universe density to critical density (1 for flat universe).
    - Omega_M: ratio of matter density to critical density.
    - Omega_Lambda: ratio of vaccum (dark) energy density to critical density.
    - Omega_R: ratio of relativistic particle energy density to critical density.
    - Omega_K: universe curvature parameter (persumed to be 0 in this project).
    - Omega_Lambda + Omega_R + Omega_M + Omega_K = Omega.
    
    When refering to the density parameters, I refer to these definitions.
    
  ### Hubble Law and Hubble Parameter
    The Hubble Law states that the farther away a galaxy is from us, the faster it appears to be moving away from us. This is represented 
    by a mathematical value known as the Hubble parameter, which measures the rate of expansion of the universe. The Hubble parameter is 
    denoted by the symbol "H" and has units of kilometers per second per megaparsec (km/s/Mpc).

    In simpler terms, the Hubble parameter tells us how fast the universe is expanding for every unit of distance. For example, if the 
    Hubble parameter is 70 km/s/Mpc (which is the standard value), it means that a galaxy that is 1 megaparsec (3.26 million light-years) 
    away from us is moving away from us at a speed of 70 kilometers per second.

    The Hubble Law and the Hubble parameter have important implications for our understanding of the universe. By measuring the distances 
    and velocities of galaxies, we can use the Hubble parameter to estimate the age of the universe and the amount of matter and energy it 
    contains.
  
  ### LSQ Fit
    LSQ (least-squares) fitting is a common method used in statistics and data analysis to find the best-fitting curve or line that 
    describes a set of data points. The LSQ fit involves minimizing the sum of the squared differences between the observed data points and 
    the values predicted by the curve or line.

    In other words, the LSQ fit tries to find the curve or line that has the smallest overall distance from the observed data points. This 
    can be done by adjusting the parameters of the curve or line until the sum of the squared differences is as small as possible. We do this 
    by creating an error function that sums the squared differences of the data points and finding the minimum point of that error function.
    
    In this project, the data points are the luminosity distance values of supernovae from SCP and their redshift.

# Project Outline
    
    In this project I represent a luminosity distance for redshift function with the Hubble and density parameters. Then, I create an error 
    function for the luminosity distance and using an LSQ fit find the values of the parameters that gives minimal error.
    

# Code

    This code defines an LSQ error function for the luminosity distance function.
    This code uses the built-in fminsearch function to find the minimum value for the LSQ error function.
    --- USE THE XLSX FILE FOR THE SUPERNOVA DATABASE AND CHANGE THE FILE LOCATION IN THE CODE ACCORDINGLY ---

### Algorithm

    Set starting values for the parameters randomly.
    Constrain the parameters for physically possible values (Relativistic particle energy density not greater than 0.1 and non negative).
    Find the closest minimum value point to those starting values.
    Store the parameter values that correspond to the minimum point.
    Repeat in a recursive manner 150 times.
    Create a mean average from the 150 results and calculate statistical error.
    Plot the luminsoity distance function given the final results.

# Deriving Basic Conclusions from the Results

  - Universe deceleration parameter (q): q = Omega_M / 2 - Omega_Lambda.
  - Age of the universe: 1/H.

## Example of a Final Luminosity Distance Function Fit
![image](https://github.com/NoRehovot/MATLAB-Cosmological-Parameter-LSQ-Fit/blob/main/final_function.png)
    
    Where the red dots are the SCP data with their statistical error plotted as errorbars and the green function is the final fit using this code.

### This project was accomplished working with Gilad Sadeh from the Weizmann Institute of Science.
