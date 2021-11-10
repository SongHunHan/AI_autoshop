
# AI_autoshop

#### 산업이 발전하면서 계산을 해주는 인력이 없어지고 무인접포가 많이 생겼다. 최근에는 AI발전으로 계산의 과정까지 없애려는 움직임이 보였고 아주 흥미로웠다.
[![gitAutoShop](https://user-images.githubusercontent.com/65228530/130751880-c6aed3c2-a81b-48b1-a2c2-a267a17fe7c1.png)](https://www.youtube.com/watch?v=yeS8TJwBAFs&t=103s)

### 상품 list
트윅스, 하리보젤리, 코카콜라, 레드불, 비누... 등등 60개의 상품List가 있다.
60개의 목록을 98000장 가량 학습 시켰다.


# 


```python
import matplotlib.pyplot as plt
import numpy as np
from glob import glob
```
<p>

```python
result_img = glob('/workspace/Docker/marchandise/ex/*.jpg')
len(result_img)
```



```python
fig=plt.figure(figsize=(40, 20))
columns = 3
rows = 3
for i in range(1, columns*rows +1):
    img = np.random.choice(result_img)
    img = plt.imread(img)
    fig.add_subplot(rows, columns, i)
    plt.imshow(img)
plt.show()
```


![Result](https://user-images.githubusercontent.com/65228530/130936141-85fb914c-4f21-4049-9345-951fed75f084.png)



```python

```

## 실제 상황에 대한 result
학습시킨 결과 비슷한 데이터에 대해서는 검출이 잘되는걸 확인했다. 실제로 classList있는 하리보, 트윅스, 코카콜라, 레드불등을 구매해서 detect해보았다.
    
<p align="center">
  <img src="https://user-images.githubusercontent.com/65228530/131086226-bd046148-0761-4ebf-8596-37f874c551e0.gif" alt="real gif1"/>
    
  <img src="https://user-images.githubusercontent.com/65228530/131086324-ddae379a-ae49-40ae-a04a-60a47dcda835.gif" alt="real gif2"/>
</p> 
# AI_autoshop
