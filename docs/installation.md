# Installation

Installing DIYABC should be easy: you just need to grab the pre-built release the best suits your platform (Windows, MacOS or Linux) from the [releases page](https://github.com/diyabc/diyabc/releases).

The file should be executable and, once you download it, you can rename it as `diyabc` and run, to test the successful installation:

```bash
# on macOS/Linux
diyabc -h
# on Windows
.\diyabc.exe -h
```

If you're not lucky, and for some reasons this first approach does not work, then you should proceed with this second approach, i.e. building the code from source, although it requires a little bit more programming and is suitable only for Linux/macOS.

- First of all, you need to check that `cmake` is installed:

```bash
cmake --version
```

- If `cmake` is not installed, then proceed to install it:

```bash
# from package resources
sudo apt-get -y install cmake # Ubuntu
# with conda
conda install -y conda-forge::cmake
# with brew
brew install cmake
```

- Once `cmake` is installed, clone DIYABC repository:

```bash
git clone --recurse-submodules https://github.com/diyabc/diyabc.git
cd diyabc
```

- Create a `build` folder

```bash
mkdir build
cd build
```

- Pre-build DIYABC

```bash
cmake ../
```

- Build DIYABC

```bash
cmake --build . --config Release
```

You will find diyabc executable under `diyabc/build/src-JMC-C++/general`

Now we can just copy the binary file in our working directory:

```bash
cd ../..
cp diyabc/build/src-JMC-C++/general diyabc
```

And we can optionally remove the diyabc repository we compiled as it is no longer necessary:

```bash
rm -rf diyabc/
```

And then we can test the installation by running:

```bash
./diyabc -h
```


With this, you should be able to successfully install DIYABC. Now, let's follow with some examples!