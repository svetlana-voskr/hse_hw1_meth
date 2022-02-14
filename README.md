# hse_hw1_meth
## Часть 1

## Часть 2
### a + b

| Образцы  | 11347700-11367700   | 40185800-40195800   | deduplication % |
|----------|------|------|-----------------|
| cell8    | 1090 | 464  | 81.69           |
| epiblast | 2328 | 1062 | 97.08           |
| ICM      | 1456 | 630  | 90.92           |

**bash - skript:** ! ls *pe.bam | xargs -P 4 -tI{} deduplicate_bismark  --bam  --paired  -o s_{} {}
### c
Выполнено
### d
HTML отчеты в [папке](\html) 
#### Epiblast

<p float="left">
  <img src="./img/Bismark M-bias Read 1_22.png" width="48%" />
  <img src="./img/Bismark M-bias Read 2_22.png" width="48%" /> 
</p>
M-bias (Read 1)             |  M-bias (Read 2) 
:-------------------------:|:-------------------------:
![alt](./img/Bismark M-bias Read 1_22.png)  |  ![alt](./img/Bismark M-bias Read 2_22.png)

#### Cell8
M-bias (Read 1)             |  M-bias (Read 2) 
:-------------------------:|:-------------------------:
![alt](./img/Bismark M-bias Read 1_73.png)  |  ![alt](./img/Bismark M-bias Read 2_73.png)

#### ICM
M-bias (Read 1)             |  M-bias (Read 2) 
:-------------------------:|:-------------------------:
![alt](./img/Bismark M-bias Read 1_75.png)  |  ![alt](./img/Bismark M-bias Read 2_75.png)
