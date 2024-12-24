# TopMGQuant
(global version)

## System requirements
GCC version higher than 4.8.2 for C++11 support

CMake (>= 3.1)

## Tutorial
**Environment requirement: Linux (Ubuntu)**

 Step 1:   Please install the following packages before running the program
    
    # install compiling tools
    sudo apt-get install build-essential cmake

    # install other library packages
    sudo apt-get install zlib1g-dev libboost-filesystem-dev \
                     libboost-program-options-dev \
                     libboost-system-dev \
                     libboost-thread-dev \
                     libboost-iostreams-dev \
                     libboost-chrono-dev \
                     libxalan-c-dev

    # install the catch unit test framework (https://github.com/philsquared/Catch)
    sudo apt-get install catch

    # install Qt5 for GUI
    sudo apt-get install qtbase5-dev

    # cd the toppic suite source folder toppic-suite-1.x.x
    # replace 1.x.x with the version number
    cd toppic-suite-1.x.x

Step 2:  Compile the program

    # build 
    mkdir build
    cd build
    cmake ..
    make -j$(nproc)

Step 3:  Add the folder toppic_resources to the folder toppic_suite_1.x.x/bin

    cd ../bin
    ln -s ../toppic_resources 

Step 4:  Run the program with the input data

    ./bin/topmg -i SimData/variable_mods.txt SimData/human_Histone_H4.fasta mixtureData/071210_070610His0Gy070210H4_H061010A_ms2.msalign
    
 Note:  Here are the input test data we used in this tutorial, you can find them in the following folders.
 
    # test data
    protein: human_Histone_H4.fasta
    spectrum: SimData/1.ms2 SimData/2.ms2
    modification: SimData/variable_mods.txt

