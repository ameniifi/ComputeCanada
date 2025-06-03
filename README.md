# ComputeCanada

salloc --gres=gpu:a100_2g.10gb:1 --time=8:00:00 --ntasks=1 --mem=8G --nodes=1

salloc --gres=gpu:a100_2g.10gb:1 --time=90:00:00 --ntasks=1 --mem=32G --nodes=1

. ~/miniconda3/bin/activate

conda activate pyskl

module load StdEnv/2020

module load python/3.7.9

module load opencv/4.5.1

cd projects

cd def-wassim

cd saf10

cd Amani

cd pyskl

## to run a model:

python run.py

## to test a model:

python tools/test.py configs/msg3d/msg3d_pyskl_ntu60_xsub_hrnet/j.py --eval mean_class_accuracy top_k_accuracy --checkpoint Amani/work_dirs/msg3d_pyskl_ntu60_xsub_hrnet/j/latest.pth

## To cancel a job

sq

Scancel jobid
