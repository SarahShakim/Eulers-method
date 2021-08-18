% Euler’s method
%
%Euler’s method finds the slope at various points to approximate a function on a graph. 
%You use an approximation to approximate the next point. Heun’s method finds the derivative
%of one point to find the next point to give a graph with a better approximation than Euler’s
%method. These methods can be used to solve an IVP of an ODE.
%
% Parameters
% ==========
%    f: The function f takes in a value of t and outputs the corresponding y value
%    t_rng :The function f takes in a value of t and outputs the corresponding y value
%    y0: The initial value that we’re using to approximate the next value
%    n: The number of intervals we want to divide “t” into
% Return Values
% =============
%    t_out : The vector tout is a row vector with n equally spaced intervals within the range
%    y_out : The vector yout is a row vector with n values that approximates the function from 2 to n
 
function [ t_out, y_out ] = euler( f, t_rng, y0, n )
 
    if ~all( size( t_rng ) == [1, 2] ) 
        throw( MException( 'MATLAB:invalid_argument', ...
        'the argument t_rng is not a 2-dimensional column vector' ) );
    end
  
    if ~isscalar( y0 ) 
        throw( MException( 'MATLAB:invalid_argument', ...
        'the argument y0 is not a scalar' ) );
    end
 
    if ~isscalar( n ) || (n <= 0) 
        throw( MException( 'MATLAB:invalid_argument', ...
        'the argument n is not a positive scalar' ) );
    end
 
    if ~isa( f, 'function_handle' )
        throw( MException( 'MATLAB:invalid_argument', ...
        'the argument f is not a function handle' ) );
    end
    
    %Determining the distance between each point using the equation
    h = (t_rng(2) - t_rng(1)) / (n - 1);
    %creates a vector of n equally spaced values between the range
    t_out = linspace (t_rng(1), t_rng(2), n);
    %Assign y_out as a vector with the first value being the initial condition
    %(y_out,1¬) and the rest of the n values 0.
    y_out = zeros(1 , n);    
    y_out(1) = y0;
    %Create a loop going from 1 to n-1 for values of K w
    for i = 1 : (n - 1) 
        %Update the value of y_out equal to the yout value from that K subtracted from the distance multiplied by K 
        y_out(:, i + 1) = y_out(:, i) + (h * f(t_out(i+1), y_out(:, i)));
    end 
 
    
 
end
