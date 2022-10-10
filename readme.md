
# C++ Valgrind exercise

## Overview 

The codes in the ```valgrind_branch``` contained memory leak and data uninitialization errors which were observed using Valgrind and rectified. 

## Running the Program
```
git clone https://github.com/adarshmalapaka/valgrind-exercise
cd <path to repository>
mkdir build
cd build
cmake ..
make
Run program: ./app/shell-app
```

### Valgrind

```
sudo apt install valgrind
cd build
valgrind --leak-check=full -v ./app/shell-app >& ../results/valgrind_rectified_result.txt
```

### KCachegrind

```
sudo apt-get install -y kcachegrind
cd build
valgrind --tool=callgrind  ./app/shell-app
kcachegrind
```

Open the ```callgrind.out.xxxx``` file in the GUI.

