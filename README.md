# createEnviroment
Conda

layout	title
default
Schedule - scRNAseq course
Conda Instructions
In this workshop you will use conda environments to run the exercises. This is because conda environments allow all students to have the save computing environment, i.e. package versions. This enforces reproducibility for you to run this material without the need to re-install or change your local versions. See and graphical example below:



Conda environments are a self-contained directory that you can use in order to reproduce all your results. 

Two of the required software are not available as Conda packages, please see the separate instructions for installing SingleR and CHETAH.

Briefly, you need to:

Install Conda and download the .yml file
Create and activate the environment
Deactivate the environment after running your analyses
You can read more about Conda environments and other important concepts to help you make your research reproducible.


Install Conda and download the environment file
You should start by installing Conda. After installing Conda, download the course Conda file and put it in your working folder.

On MacOSX
curl -o Miniconda3-latest-MacOSX-x86_64.sh https://repo.anaconda.com/anaconda/Anaconda-latest-Linux-x86_64.sh
sh Miniconda3-latest-MacOSX-x86_64.sh
Follow the instructions on screen replying yes when necessary. Restart your terminal window to apply modifications.

On Ubuntu
wget https://repo.anaconda.com/anaconda/Anaconda-latest-Linux-x86_64.sh
sh Miniconda3-latest-Linux-x86_64.sh
Follow the instructions on screen replying yes when necessary. Restart your terminal window to apply modifications.

On Windows10
Several packages are not available for Windows. However, on windows10 we can run a Ubuntu subsystem to overcome this issue. Please follow the instructions Alternative option on Windows (WLS) below to install it.

current version: 22.9.0
conda update -n base -c defaults conda
export PATH=~/anaconda3/bin:$PATH


Create a Conda environment from file
To download the environment_r.yml file using the command on Terminal:

#Ubuntu
wget https://anaconda.org/jsandhu/environment.yml/2016.11.09.1045/download/environment.yml

#MacOSX
curl -o https://anaconda.org/jsandhu/environment.yml/2016.11.09.1045/download/environment.yml

After this, you should have a file named environment_r.yml in your directory (it does not matter where, you can save on Downloads folder for example). Next, type:

conda env create -p scRNAseq -f environment.yml

Several messages will show up on your screen and will tell you about the installation process. This may take a few minutes depending on how many packages are to be installed.

Downloading and Extracting Packages
intel-openmp-2023.0. | 15.1 MB   | ##################################### | 100% 
more-itertools-5.0.0 | 89 KB     | ##################################### | 100% 
contextlib2-0.6.0.po | 13 KB     | ##################################### | 100% 
netcdf4-1.4.2        | 453 KB    | ##################################### | 100% 
mkl-2020.2           | 138.3 MB  | ##################################### | 100% 
krb5-1.19.4          | 1.3 MB    | ##################################### | 100% 
c-ares-1.19.0        | 118 KB    | ##################################### | 100% 
sqlite-3.41.1        | 1.2 MB    | ##################################### | 100% 
jpeg-9e              | 262 KB    | ##################################### | 100% 
pip-19.3.1           | 1.7 MB    | ##################################### | 100% 
libnetcdf-4.6.1      | 833 KB    | ##################################### | 100% 
packaging-20.9       | 37 KB     | ##################################### | 100% 
pathlib2-2.3.5       | 37 KB     | ##################################### | 100% 
hdf4-4.2.13          | 714 KB    | ##################################### | 100% 
openssl-1.1.1t       | 3.7 MB    | ##################################### | 100% 
scandir-1.10.0       | 15 KB     | ##################################### | 100% 
python-2.7.18        | 11.3 MB   | ##################################### | 100% 
ca-certificates-2023 | 120 KB    | ##################################### | 100% 
pytest-4.6.2         | 355 KB    | ##################################### | 100% 
curl-7.88.1          | 88 KB     | ##################################### | 100% 
mkl_random-1.1.0     | 297 KB    | ##################################### | 100% 
numpy-base-1.16.6    | 3.5 MB    | ##################################### | 100% 
importlib_metadata-1 | 46 KB     | ##################################### | 100% 
zlib-1.2.13          | 103 KB    | ##################################### | 100% 
pyparsing-2.4.7      | 59 KB     | ##################################### | 100% 
libcurl-7.88.1       | 383 KB    | ##################################### | 100% 
libedit-3.1.20221030 | 181 KB    | ##################################### | 100% 
configparser-4.0.2   | 43 KB     | ##################################### | 100% 
ncurses-6.4          | 914 KB    | ##################################### | 100% 
certifi-2020.6.20    | 155 KB    | ##################################### | 100% 
mkl_fft-1.0.15       | 146 KB    | ##################################### | 100% 
libffi-3.4.2         | 136 KB    | ##################################### | 100% 
pluggy-0.13.1        | 33 KB     | ##################################### | 100% 
cftime-1.0.4.2       | 272 KB    | ##################################### | 100% 
readline-8.2         | 357 KB    | ##################################### | 100% 
libgfortran4-7.5.0   | 995 KB    | ##################################### | 100% 
zipp-0.6.0           | 9 KB      | ##################################### | 100% 
mkl-service-2.3.0    | 217 KB    | ##################################### | 100% 
funcsigs-1.0.2       | 22 KB     | ##################################### | 100% 
cython-0.29.14       | 2.0 MB    | ##################################### | 100% 
numpy-1.16.6         | 48 KB     | ##################################### | 100% 
hdf5-1.10.4          | 3.9 MB    | ##################################### | 100% 
setuptools-44.0.0    | 512 KB    | ##################################### | 100% 
py-1.10.0            | 76 KB     | ##################################### | 100% 
libgfortran-ng-7.5.0 | 22 KB     | ##################################### | 100% 
Preparing transaction: done
Verifying transaction: done
Executing transaction: done


Activate the environment
Once the environment is created, we need to activate it in order to use the softwares and packages inside it. To activate an environment type:

conda activate /home/mayte/software/scRNAseq

source activate 
From this point on you can run any of the contents from the course. For instance, you can directly launch RStudio by typing rstudio. Here it is important to add the & symbol in the end to be able to use the command line at the same time if needed. You can open other files from Rstudio later as well.

source activate /home/mayte/software/scRNAseq

rstudio ./labs/compiled/my_script.Rmd &

Deactivate the environment
After you've ran all your analyses, you can deactivate the environment by typing:

conda deactivate

sudo apt-get update
sudo apt-get install libgl1-mesa-glx libegl1-mesa libxrandr2 libxrandr2 libxss1 libxcursor1 libxcomposite1 libasound2 libxi6 libxtst6
