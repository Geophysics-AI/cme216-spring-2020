---
layout: page
title: Installation Guide For ADCME 
---

ADCME is tested and supported on Linux or MacOS system. The support for custom operators on Windows is not available yet. We have separate instructions for MacOS and Linux systems. 

If you only have a windows machine, you can use the Stanford [farmshare](https://srcc.stanford.edu/farmshare2) computing environment. SSH to `rice.stanford.edu` using your SUNetID.

# Install ADCME

## 1. Install Julia

### For MacOS

Due to an incompatability issue of the latest Julia (1.4) and TensorFlow 1.x, please download and install Julia 1.3 from the [official website](https://julialang.org/downloads/oldreleases/#v131_dec_30_2019). 

After installation, Julia-1.3 will appear in your `Application` folder. Open the Julia application and you will see the Julia prompt

```julia
julia> Sys.BINDIR
```

Example output:

```bash
"/Applications/Julia-1.3.app/Contents/Resources/julia/bin"
```

Add this path to your `PATH` environment variable

```bash
echo 'export PATH=/Applications/Julia-1.3.app/Contents/Resources/julia/bin:$PATH' >>~/.bash_profile
```

### For Linux 

Download Julia 1.3 or 1.4 from the [official website](https://julialang.org/downloads/). Uncompress the tarball to any directory you want. There is a directory `bin` inside the Julia directory you just uncompressed. Add the absolute path of the `bin` directory to your `PATH` environment variable. 


---

Example:

**Linux**

```bash
echo 'export PATH=:$PATH' >>~/.bashrc
```

Then refresh your environment by running

```bash
source ~/.bashrc
```

**Mac**

```bash
echo 'export PATH=:$PATH' >>~/.bash_profile
```

Then refresh your environment by running

```bash
source ~/.bash_profile
```

---

Type `julia` in the terminal, and you should be able to open a Julia prompt. 


Open a new terminal and type `julia`. You should see a `julia` prompt.

## 2. Install Project Dependencies

This homework requires installing some Julia packages. Open your julia 

```bash
$ julia
```

and type

```julia
julia> using Pkg
julia> Pkg.add("ADCME")
julia> Pkg.add("DelimitedFiles")
julia> Pkg.add("PyCall")
julia> Pkg.add("PyPlot")
```

This will take up to 10 minutes for the first time. 

## 3. Start using ADCME

Now you can start using ADCME (ignore the warnings; they will disappear next time)

```julia
julia> using ADCME
julia> a = constant(ones(5,5))
julia> b = a * ones(5)
julia> sess = Session(); init(sess)
julia> run(sess, b)
```

Expected output:

```bash
5-element Array{Float64,1}:
 5.0
 5.0
 5.0
 5.0
 5.0
```


## 4. Test Custom Operator Support

In the homework we will use custom operators. To test whether your installation works for custom operators, try

```julia
julia> using ADCME
julia> ADCME.precompile()
```

If you encounter any compilation issue, you can report in Slack channel. 


# Compare the Custom Operator for 2D Case

This guide explains how to compile the custom operator for the 2D Case. 

In `2DCase`, you have two source files: `HeatEquation.h` and `HeatEquation.cpp`. You need to compile them into a shared library, which you can use in the inverse modeling. To do so, go into `2DCase` directory and open a Julia prompt in a terminal. 

```julia
julia> using ADCME
julia> mkdir("build")
julia> cd("build")
julia> ADCME.cmake()
julia> ADCME.make()
```

You will see there is a `libHeatEquation.dylib` (MacOS) or `libHeatEquation.so` (Linux) in your `build` directory. 

Run the `Case2D/example.jl` file to check if the shared library works. 