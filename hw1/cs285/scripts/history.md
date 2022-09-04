# Commands for reproducing results:

# Q1

## Ant-v4: achieved high Eval_AverageReturn! Change seed from 1 -> 3.
```python
python cs285/scripts/run_hw1.py \
--expert_policy_file cs285/policies/experts/Ant.pkl \
--env_name Ant-v4 --exp_name bc_ant --n_iter 1 \
--expert_data cs285/expert_data/expert_data_Ant-v4.pkl \
--video_log_freq -1 --eval_batch_size 5000 --ep_len 1000 --seed 1
```

## Walker2d: poor performance! Change seed from 1 -> 3.

```python
python cs285/scripts/run_hw1.py \
--expert_policy_file cs285/policies/experts/Walker2d.pkl \
--env_name Walker2d-v4 --exp_name bc_walker --n_iter 1 \
--expert_data cs285/expert_data/expert_data_Walker2d-v4.pkl \
--video_log_freq -1 --eval_batch_size 5000 --ep_len 1000 --seed 1
```

## hyperparameter: Change size from 4 -> 64

```python
python cs285/scripts/run_hw1.py \
--expert_policy_file cs285/policies/experts/Ant.pkl \
--env_name Ant-v4 --exp_name bc_ant --n_iter 1 \
--expert_data cs285/expert_data/expert_data_Ant-v4.pkl \
--video_log_freq -1 --eval_batch_size 5000 --ep_len 1000 --seed 1 --size 16
```

# Q2

## Ant
```python
python cs285/scripts/run_hw1.py \
--expert_policy_file cs285/policies/experts/Ant.pkl \
--env_name Ant-v4 --exp_name dagger_ant --n_iter 10 \
--expert_data cs285/expert_data/expert_data_Ant-v4.pkl \
--video_log_freq -1 --do_dagger --eval_batch_size 5000 --ep_len 1000
```

## Walker2d
```python
python cs285/scripts/run_hw1.py \
--expert_policy_file cs285/policies/experts/Walker2d.pkl \
--env_name Walker2d-v4 --exp_name dagger_walker --n_iter 10 \
--expert_data cs285/expert_data/expert_data_Walker2d-v4.pkl \
--video_log_freq -1 --do_dagger --eval_batch_size 5000 --ep_len 1000 --seed 1
```

