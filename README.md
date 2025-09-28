# DCVLR-baseline
starter_kit https://github.com/oumi-ai/oumi/tree/main/configs/projects/dcvlr

## Fast Start:
1. Install "GitHub Desktop"
2. Click Code -> Open with GitHub Desktop
3. Create issue-xxx branch
4. Do your changes with favorite IDE
5. Commit to issue-xxx branch
6. Push origin
7. Create Pull Request to main branch
8. Merge Pull Request or ask for review

## Deployment:

- Register on Lambda Labs https://lambdalabs.com/ and get credits
Create instance when you ready to run https://docs.lambda.ai/education/
Run from IDE [How to connect Lambdalabs to Pycharm via SSH](https://medium.com/@val.mannucci/how-to-connect-lambdalabs-to-pycharm-via-ssh-85fca2b49a60)

or

- KOA HPC https://koa.its.hawaii.edu/

connect to KOA
ssh USERNAME@koa.its.hawaii.edu

you are at login session [USERNAME@login-0102 ~]$
allocate resources and run bash terminal on it. Adjust (see avaliable shared resourses 'sinfo -p gpu,gpu-sandbox,kill-shared | grep gpu' ) how much you think you need and -t time:

'srun  -p sandbox -c 2 --mem=6G -t 10 --pty /bin/bash' 
        or another example 
'srun -I30 -p kill-shared -N 1 -c 3 --mem=8G -t 2-00:00:00 --gres=gpu:NV-V100-SXM2:1 --pty /bin/bash'

you are at compute node [USERNAME@cn-03-13-04 ~]$ ready to run a load
'python --version' 

load anaconda as a module and activate enviroment

'module load lang/Anaconda3
source activate base'

Now can install modules with pip

[more](https://uhawaii.atlassian.net/wiki/spaces/HPC/pages/430407800/How+to+Request+GPUs+on+Koa) [info](https://docs.google.com/document/d/1h00x2pAjIjMDJ-1RBeHQaTvnfxUhM_lAVNbskEc9f7A/edit?usp=sharing)

or

- Google Colab Pro https://colab.research.google.com/
limited by a browser session

or

- Run locally 
limited by your hardware

## Project management:

We can use Issue Driven Project Management (IDPM) convenience (not necessary):

- Use GitHub Projects to create issues and track tasks
- Add issue-xxx (xxx - number of the issue provided by GitHub ex. issue-001) to the name
- Create branch issue-xxx from main branch to work on it
- Do not commit to main branch directly, only merge with Pull Request.
