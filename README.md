# Market-Analysis-Report-for-National-Clothing-Chain
`Udacity Project`

## Linear regression
Linear Regression method helps us to find whether the relationship among X variable(Independent) & Y variable(Dependent) is exists & level of effect.
here 
- Postive relationship (X increase leads to Y increase)
- Negative relationnship (X increase leads to Y decrease)

eg: customers income level vs purchases of products

- R = correlation Cofficient(ranges from -1 to 1),
- R^2 = Coefficient of Determination(ranges from 0 to 1)


`correlation b/w avg. income by state & last 6 months avg. purchase by customers`

![image](https://user-images.githubusercontent.com/92777166/138555048-b1fc953a-bc3e-4cb0-bc71-6210e7b809fe.png)

`*Coefficient of Determination = 0.78**`

```
Using Quick measure 
Under Mathematical operations - correlation Cofficient(R)
then applying square to R
that is R^2 = Coefficient of Determination
```
<br /> 

Now I will show you equation which is helpful to predict the future sales by customer income

using 
`y = mx + b` 

![image](https://user-images.githubusercontent.com/92777166/138557613-fced9245-814d-4fc5-a599-fa0cf781e7ef.png)


![image](https://user-images.githubusercontent.com/92777166/138558516-8a6cdfb4-fad5-40d6-b90d-5bd134cde0a7.png)


```
y = mx +b
n = number of rows
x = the variable x you input

m = [n x (sum of xy) - (sum of x) * (sum of y)] / [ n * (sum of x^2) - (sum of x)^2]

b = [ (sum of y) * (sum of x^2) - (sum of x) (sum of xy)] / [ n * (sum of x^2) - (sum of x)^2]
```

**`m = 0.010726`**
**`b = 722.14`**

Now using the equation we can predict the purchases from customers depends on there income level.

eg: if the Avg. income level(X) = 150k

then avg. purchases(y) we predict = 0.010726(150k) + (-722.14) = **886.8**   **`y = mx + b`**

---

## customer Income Bin

![image](https://user-images.githubusercontent.com/92777166/138559884-a7a3f582-773b-47a3-9cb4-5d5cc7e88f01.png)

`DAX`
```dax
Customer Income Bin = 

IF([Predicated Income X]<50000,0,

IF([Predicated Income X]>=50000 && [Predicated Income X]<100000,50000,

IF([Predicated Income X]>=100000 && [Predicated Income X]<150000,100000,

IF([Predicated Income X]>=150000 && [Predicated Income X]<200000,150000,

IF([Predicated Income X]>=200000 && [Predicated Income X]<250000,200000,

IF([Predicated Income X]>=250000 && [Predicated Income X]<300000,250000,

IF([Predicated Income X]>=300000 && [Predicated Income X]<350000,300000,

IF([Predicated Income X]>=350000 && [Predicated Income X]<400000,350000,

IF([Predicated Income X]>40000,400000,0

)))))))))
```
*we can use `SWITCH` function*

---
## customer raing vs returns

![image](https://user-images.githubusercontent.com/92777166/138560184-ae0752e6-ca3c-4ac7-a73a-aec60ac435e6.png)

`*Coefficient of Determination = 0.69**`

---



