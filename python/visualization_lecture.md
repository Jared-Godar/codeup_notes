# Matplotlib

- Matplotlib FuncAnimation
    - Creat fix  axes
    - Updatge

- Particle in a box
    - initial poition
    - Vo
    - Define boundaries
    - many particles
        - Random initial state
        - Random initial velocity
            - Find pairs of particles collision
            - Update velocity of coliding pairs
        - Add gravity
- Epidemic Simulations and Visualizations
    - Visualization
        - Dot per person
    - Variabiles
        - r
        - Duration
        - Distancing 
        - Travel
# Matplotlib

- Two APIs / interfaces
    1. `pyplot` from matlab world
        - Interactive plots
        - Simple cases of programattic plot generation
    2. Object-oriented API
        - More control and customization of your plots

## Line and Scatter Charts

- Convention is to import the `pyplot` module as `plt`

    `import matplotlib.pyplot as plt`

    `print(plt)`

    `<module 'matplotlib.pyplot' from '/Users/plan9/matplotlib/lib/matplotlib/pyplot.py'>`

## Line Charts

- For the most basic example, we can create a sequence of numbers, then a chart (calling .`plot`), then call the `.show` method to display it.

- Note that the act of creating the chart and showing it are two separate acts.

    x = list(range(150))

    plt.plot(x)
    plt.show()

