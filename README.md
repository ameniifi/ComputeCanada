# ComputeCanada

salloc --gres=gpu:a100_2g.10gb:1 --time=8:00:00 --ntasks=1 --mem=8G --nodes=1

. ~/miniconda3/bin/activate

conda activate pyskl

module load StdEnv/2020

module load python/3.7.9

module load opencv/4.5.1
