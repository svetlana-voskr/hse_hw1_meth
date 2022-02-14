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

#### Cell8
<p float="left">
  <img src="./img/Bismark M-bias Read 1_73.png" width="49%" />
  <img src="./img/Bismark M-bias Read 2_73.png" width="49%" /> 
</p>

#### Epiblast

<p float="left">
  <img src="./img/Bismark M-bias Read 1_22.png" width="49%" />
  <img src="./img/Bismark M-bias Read 2_22.png" width="49%" /> 
</p>


#### ICM
<p float="left">
  <img src="./img/Bismark M-bias Read 1_75.png" width="49%" />
  <img src="./img/Bismark M-bias Read 2_75.png" width="49%" /> 
</p>

### f
Код:
```
names = ['3824222', '5836473', '5836475']
for kod in names:
  name = 's_SRR' + kod + '_1_bismark_bt2_pe.deduplicated.bedGraph'
  a = pd.read_csv(name, delimiter='\t', skiprows=1, header=None)
  fig = plt.figure(figsize=(15, 5))
  plt.title('Распределение метилирования для %s' % kod, fontsize=20) 
  plt.hist(a[3], bins=100, density=True)
  plt.xlabel('Процент метилированных цитозинов')
  plt.ylabel('Частота')
  plt.show()
  fig.savefig('%s.png' % kod)
```
#### Cell8
![](./img/5836473.png)

#### Epiblast
![](./img/3824222.png)

#### ICM
![](./img/5836475.png)

)
