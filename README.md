# Eulers-method

## Euler's method finds the slope at various points to approximate a function on a graph. This approximation is used to approximate the next point. Heun's method finds the derivative of a pont to find the next point to create a graph with a better approximation than Euler's method. Both of these methods can be used to solve and IVP of and ODE.

Parameters

f: The function f takes in a value of t and outputs the corresponding y value

t_rng :The function f takes in a value of t and outputs the corresponding y value

y0: The initial value that we’re using to approximate the next value

n: The number of intervals we want to divide “t” into

To find the solution, I had to fisrt determie the distance between each point using the equation h = (t_final - t_0)/n-1. 
Then, given the initial and final values of t, I had to find the vector 9of the n equally spaced numbers and assign it to t_out.
Next, I had to assign y_out as a vector with the first value being the initial condition (y_out,1) and the rest of the n values to 0.
Now a loop was created going from 1 to n-1 for valus of K where:
- the slope of K was found
- the corresponding t_out and y_out values were found
- updated the valuued of y_out(y_out, K+1) equal to the y_out value from that K subtracted from the distance multiplied by K(y_out,K+1 = y_out _x_ (h(K))


**Example: finding the approximation of the IVP y(1)(t) = f3b(t, y(t)) with y(0) = 0**
![image](https://user-images.githubusercontent.com/58648072/129954574-c5be6813-cb87-47ec-a381-bd39843e2ab2.png)
