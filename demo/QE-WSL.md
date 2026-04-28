# QE installation  WSL.2

- Update your ubuntu

```bash
sudo apt update
```

- Install required libraries

```bash
sudo apt install autoconf build-essential gfortran libblas3 libc6 libfftw3-dev liblapack-dev 
sudo apt install libopenmpi-dev libscalapack-openmpi-dev libelpa-dev
```



---------------



## QE Download & Compile

- Download  last version of QE from gitlab repository

```bash
mkdir SOURCES
cd SOURCES
wget https://gitlab.com/QEF/q-e/-/archive/qe-7.4/q-e-qe-7.4.tar.gz
tar -xvf q-e-qe-7.4.tar.gz
```



- Config  and make 

  ```
  ./configure
  make pw
  make pp
  make ph
  
  
  ```
  
- Export PATH

  add this lines to your ~/.bashrc or ~/.zshrc 

  ```bash
  export PATH=$PATH:/home/wsluser/SOURCE/q-e-qe-7.4/bin
  ```

  

--------------------------

## Download  example files  and Run  an example

- Download  from repo

  ```bash
  wget https://github.com/Yavar-Azar/QE-Examples/archive/refs/heads/master.zip
  ```

- ###### Start your  first

  ```
  unzip master.zip
  cd QE-Examples-master/Example-01/
  mpirun -np 2 pw.x < espresso.in | tee espresso.out
  ```

  



