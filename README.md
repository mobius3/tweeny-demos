# Tweeny Demos

This project contains demo code to showcase some of the [Tweeny] features, and
some extra code to support them.

All code lives inside the `src/` folder.

## The *easings* demo

It outputs in the console all easing curves that come bundled in Tweeny. It
waits for you to press the `RETURN` before showing the next curve.

## The *loop* demo

Shows how different types of loops can be implemented via callbacks. It also
showcases some of the callback types you can use (functos, functions, lambdas,
etc).

## The *multitype* demo

Showcases how can you interpolate hetergoneous values in a single tween.

# Getting started

1. To build the demo code you should first clone this repository and its
submodules. It can be done with a single command:
```
git clone --recursive https://github.com/mobius3/tweeny-demos.git
```
2. Create a build folder inside it:
```
cd tweeny-temos
mkdir build
```
3. Execute `cmake` inside:
```
cd build
cmake ...
```

4. Build the example you want to see:
```
make easings
```

5. The built code will be available under the `build/src` folder, to execute it:
```
./src/easings
```

This process might be different on Windows platform, specially when executing
setp *3*. I recommend using the `cmake-gui` command.

# Contributing

If you have an idea for a demo, you are welcome to submit a pull request. See
the [tweeny repository] for instructions on code style.


[Tweeny]: mobius3.github.io/tweeny
[tweeny repository]: github.com/mobius3/tweeny