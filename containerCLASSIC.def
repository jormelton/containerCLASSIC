Bootstrap:docker
From:ubuntu:latest

%labels
MAINTAINER Joe Melton, ECCC

%environment
BASE_DIR=/code
export BASE_DIR

%runscript
cd /code/classctem
echo "The container is running!"

%post
mkdir -p /code
cd /code
apt update
apt install vim make libnetcdff-dev git gfortran netcdf-bin nano -y -f -m
git clone git@gitlab.com:jormelton/classctem.git
cd classctem
make
cd ..
chmod -R 777 classctem
