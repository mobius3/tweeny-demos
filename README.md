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

To build the demo code you should first clone this repository and its
submodules. It can be done with a single command:
```
git clone --recursive https://github.com/mobius3/tweeny-demos.git
```

If you decide to download an archive of this repository (as opposed of
cloning it), be sure to also download `tweeny` and put it inside the
`libs/tweeny` folder.


### Linux, MacOS and Unix

1. Create a build folder inside the newly cloned repository:
```
cd tweeny-temos
mkdir build
```
2. Execute `cmake` inside:
```
cd build
cmake ...
```

3. Build the example you want to see:
```
make easings
```

4. The built code will be available under the `build/src` folder, to execute it:
```
./src/easings
```

### Windows

1. Open CMake GUI and select the top level directory of tweeny as source
2. Select or create a build folder (it can be inside of tweeny)
3. Select the generator (depending on your compiler/IDE)
4. Click GENERATE
5. Open the generated project in your IDE, select the target and run it from there.

# Contributing

If you have an idea for a demo, you are welcome to submit a pull request. See
the [tweeny repository] for instructions on code style.

[Tweeny]: mobius3.github.io/tweeny
[tweeny repository]: github.com/mobius3/tweeny