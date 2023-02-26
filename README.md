---
author: Nhóm 2
date: 2022-06-05
generator: pandoc
title: Report-DataMing
viewport: width=device-width, initial-scale=1
---

::: {.container-fluid .main-container}
::: {#header}
# Report-DataMing {#report-dataming .title .toc-ignore}

#### Nhóm 2 {#nhóm-2 .author}

#### 2022-06-05 {#section .date}
:::

::: {#finalproject_telecommunication .section .level1}
# FinalProject_Telecommunication

::: {#dataset .section .level2}
## DataSet

    ##   customerID           gender          SeniorCitizen      Partner         
    ##  Length:7043        Length:7043        Min.   :0.0000   Length:7043       
    ##  Class :character   Class :character   1st Qu.:0.0000   Class :character  
    ##  Mode  :character   Mode  :character   Median :0.0000   Mode  :character  
    ##                                        Mean   :0.1621                     
    ##                                        3rd Qu.:0.0000                     
    ##                                        Max.   :1.0000                     
    ##                                                                           
    ##   Dependents            tenure      PhoneService       MultipleLines     
    ##  Length:7043        Min.   : 0.00   Length:7043        Length:7043       
    ##  Class :character   1st Qu.: 9.00   Class :character   Class :character  
    ##  Mode  :character   Median :29.00   Mode  :character   Mode  :character  
    ##                     Mean   :32.37                                        
    ##                     3rd Qu.:55.00                                        
    ##                     Max.   :72.00                                        
    ##                                                                          
    ##  InternetService    OnlineSecurity     OnlineBackup       DeviceProtection  
    ##  Length:7043        Length:7043        Length:7043        Length:7043       
    ##  Class :character   Class :character   Class :character   Class :character  
    ##  Mode  :character   Mode  :character   Mode  :character   Mode  :character  
    ##                                                                             
    ##                                                                             
    ##                                                                             
    ##                                                                             
    ##  TechSupport        StreamingTV        StreamingMovies      Contract        
    ##  Length:7043        Length:7043        Length:7043        Length:7043       
    ##  Class :character   Class :character   Class :character   Class :character  
    ##  Mode  :character   Mode  :character   Mode  :character   Mode  :character  
    ##                                                                             
    ##                                                                             
    ##                                                                             
    ##                                                                             
    ##  PaperlessBilling   PaymentMethod      MonthlyCharges    TotalCharges   
    ##  Length:7043        Length:7043        Min.   : 18.25   Min.   :  18.8  
    ##  Class :character   Class :character   1st Qu.: 35.50   1st Qu.: 401.4  
    ##  Mode  :character   Mode  :character   Median : 70.35   Median :1397.5  
    ##                                        Mean   : 64.76   Mean   :2283.3  
    ##                                        3rd Qu.: 89.85   3rd Qu.:3794.7  
    ##                                        Max.   :118.75   Max.   :8684.8  
    ##                                                         NA's   :11      
    ##     Churn          
    ##  Length:7043       
    ##  Class :character  
    ##  Mode  :character  
    ##                    
    ##                    
    ##                    
    ## 

#head of data

    ##   customerID gender SeniorCitizen Partner Dependents tenure PhoneService
    ## 1 7590-VHVEG Female             0     Yes         No      1           No
    ## 2 5575-GNVDE   Male             0      No         No     34          Yes
    ## 3 3668-QPYBK   Male             0      No         No      2          Yes
    ## 4 7795-CFOCW   Male             0      No         No     45           No
    ## 5 9237-HQITU Female             0      No         No      2          Yes
    ## 6 9305-CDSKC Female             0      No         No      8          Yes
    ##      MultipleLines InternetService OnlineSecurity OnlineBackup DeviceProtection
    ## 1 No phone service             DSL             No          Yes               No
    ## 2               No             DSL            Yes           No              Yes
    ## 3               No             DSL            Yes          Yes               No
    ## 4 No phone service             DSL            Yes           No              Yes
    ## 5               No     Fiber optic             No           No               No
    ## 6              Yes     Fiber optic             No           No              Yes
    ##   TechSupport StreamingTV StreamingMovies       Contract PaperlessBilling
    ## 1          No          No              No Month-to-month              Yes
    ## 2          No          No              No       One year               No
    ## 3          No          No              No Month-to-month              Yes
    ## 4         Yes          No              No       One year               No
    ## 5          No          No              No Month-to-month              Yes
    ## 6          No         Yes             Yes Month-to-month              Yes
    ##               PaymentMethod MonthlyCharges TotalCharges Churn
    ## 1          Electronic check          29.85        29.85    No
    ## 2              Mailed check          56.95      1889.50    No
    ## 3              Mailed check          53.85       108.15   Yes
    ## 4 Bank transfer (automatic)          42.30      1840.75    No
    ## 5          Electronic check          70.70       151.65   Yes
    ## 6          Electronic check          99.65       820.50   Yes
:::
:::

::: {#num-of-rows .section .level1}
# num of rows

    ## [1] 7043

#num of columns

    ## [1] 21

::: {#decsion-tree .section .level2}
## Decsion Tree

::: {#reprocessing .section .level3}
### reprocessing

> **Check NA**

    ## Warning: `funs()` was deprecated in dplyr 0.8.0.
    ## ℹ Please use a list of either functions or lambdas:
    ## 
    ## # Simple named list: list(mean = mean, median = median)
    ## 
    ## # Auto named with `tibble::lst()`: tibble::lst(mean, median)
    ## 
    ## # Using lambdas list(~ mean(., trim = .2), ~ median(., na.rm = TRUE))

    ##         ColumnTitle NAs
    ## 1        customerID   0
    ## 2            gender   0
    ## 3     SeniorCitizen   0
    ## 4           Partner   0
    ## 5        Dependents   0
    ## 6            tenure   0
    ## 7      PhoneService   0
    ## 8     MultipleLines   0
    ## 9   InternetService   0
    ## 10   OnlineSecurity   0
    ## 11     OnlineBackup   0
    ## 12 DeviceProtection   0
    ## 13      TechSupport   0
    ## 14      StreamingTV   0
    ## 15  StreamingMovies   0
    ## 16         Contract   0
    ## 17 PaperlessBilling   0
    ## 18    PaymentMethod   0
    ## 19   MonthlyCharges   0
    ## 20     TotalCharges  11
    ## 21            Churn   0

> Remove NA have NA

> Convert SeniorCitizen column 0, 1 to logical

    ## 'data.frame':    7032 obs. of  21 variables:
    ##  $ customerID      : chr  "7590-VHVEG" "5575-GNVDE" "3668-QPYBK" "7795-CFOCW" ...
    ##  $ gender          : chr  "Female" "Male" "Male" "Male" ...
    ##  $ SeniorCitizen   : logi  FALSE FALSE FALSE FALSE FALSE FALSE ...
    ##  $ Partner         : chr  "Yes" "No" "No" "No" ...
    ##  $ Dependents      : chr  "No" "No" "No" "No" ...
    ##  $ tenure          : int  1 34 2 45 2 8 22 10 28 62 ...
    ##  $ PhoneService    : chr  "No" "Yes" "Yes" "No" ...
    ##  $ MultipleLines   : chr  "No phone service" "No" "No" "No phone service" ...
    ##  $ InternetService : chr  "DSL" "DSL" "DSL" "DSL" ...
    ##  $ OnlineSecurity  : chr  "No" "Yes" "Yes" "Yes" ...
    ##  $ OnlineBackup    : chr  "Yes" "No" "Yes" "No" ...
    ##  $ DeviceProtection: chr  "No" "Yes" "No" "Yes" ...
    ##  $ TechSupport     : chr  "No" "No" "No" "Yes" ...
    ##  $ StreamingTV     : chr  "No" "No" "No" "No" ...
    ##  $ StreamingMovies : chr  "No" "No" "No" "No" ...
    ##  $ Contract        : chr  "Month-to-month" "One year" "Month-to-month" "One year" ...
    ##  $ PaperlessBilling: chr  "Yes" "No" "Yes" "No" ...
    ##  $ PaymentMethod   : chr  "Electronic check" "Mailed check" "Mailed check" "Bank transfer (automatic)" ...
    ##  $ MonthlyCharges  : num  29.9 57 53.9 42.3 70.7 ...
    ##  $ TotalCharges    : num  29.9 1889.5 108.2 1840.8 151.7 ...
    ##  $ Churn           : chr  "No" "No" "Yes" "No" ...

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/c5fe63c931763f5b8a5489e0646dd4d63fdbf764.png){width="672"}

> From the results, we see that the variable tenure and TotalCharges
> have a high correlation Remove TotalCharges.
:::
:::

::: {#model .section .level2}
## 2.1.2 Model

    ## Warning: Using an external vector in selections was deprecated in tidyselect 1.1.0.
    ## ℹ Please use `all_of()` or `any_of()` instead.
    ##   # Was:
    ##   data %>% select(cname)
    ## 
    ##   # Now:
    ##   data %>% select(all_of(cname))
    ## 
    ## See <https://tidyselect.r-lib.org/reference/faq-external-vector.html>.

    ## `summarise()` has grouped output by 'gender'. You can override using the
    ## `.groups` argument.

    ## Warning: `aes_string()` was deprecated in ggplot2 3.0.0.
    ## ℹ Please use tidy evaluation ideoms with `aes()`

    ## `summarise()` has grouped output by 'SeniorCitizen'. You can override using the
    ## `.groups` argument.

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/5ff39d63a12105e5c500b4ca97ea343bab1c6b88.png){width="672"}

    ## `summarise()` has grouped output by 'Partner'. You can override using the
    ## `.groups` argument.

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/131bc85a857d66851d1c7b3b6ddb0a22932ffac8.png){width="672"}

    ## `summarise()` has grouped output by 'Dependents'. You can override using the
    ## `.groups` argument.

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/738b0aed65acd08b7682f29e7c68cbd263465aa3.png){width="672"}

    ## `summarise()` has grouped output by 'PhoneService'. You can override using the
    ## `.groups` argument.

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/4fee947ff64e4a84e9a4e845f49cdcfe1088eb6c.png){width="672"}

    ## `summarise()` has grouped output by 'MultipleLines'. You can override using the
    ## `.groups` argument.

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/19de08aad55284b264c303d8fa9aa9eb3e31400d.png){width="672"}

    ## `summarise()` has grouped output by 'InternetService'. You can override using
    ## the `.groups` argument.

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/b9c024789818a537f10c9e583932d207896a8d87.png){width="672"}

    ## `summarise()` has grouped output by 'OnlineSecurity'. You can override using
    ## the `.groups` argument.

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/b6a6157f98670fd2a5887b6fac0e591610ab2aa4.png){width="672"}

    ## `summarise()` has grouped output by 'OnlineBackup'. You can override using the
    ## `.groups` argument.

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/f51b100250ea28445032dd64133da8c5079e2cc2.png){width="672"}

    ## `summarise()` has grouped output by 'DeviceProtection'. You can override using
    ## the `.groups` argument.

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/a5037228acaf6750255f3b1b0b490a5dd6434281.png){width="672"}

    ## `summarise()` has grouped output by 'TechSupport'. You can override using the
    ## `.groups` argument.

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/63df3f20235bbb9845798091462276a45fa6d102.png){width="672"}

    ## `summarise()` has grouped output by 'StreamingTV'. You can override using the
    ## `.groups` argument.

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/ad44b68db7a0497e40eb8618c742d36b230fb23d.png){width="672"}

    ## `summarise()` has grouped output by 'StreamingMovies'. You can override using
    ## the `.groups` argument.

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/850232803d66342ee4261f699145b0773c7fdf10.png){width="672"}

    ## `summarise()` has grouped output by 'Contract'. You can override using the
    ## `.groups` argument.

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/886fc41c9b07621d450d468333c7a590aff9089e.png){width="672"}

    ## `summarise()` has grouped output by 'PaperlessBilling'. You can override using
    ## the `.groups` argument.

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/d904d83b7298818b2374ba254ca05c361ca0d203.png){width="672"}

    ## `summarise()` has grouped output by 'PaymentMethod'. You can override using the
    ## `.groups` argument.

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/65881d4c7578812e48a36001f75b4c36360f8111.png){width="672"}![](vertopal_13072b7bdc7249c89d6eab327256fbc8/71664f467794d71e2d593f255cb91424b8105333.png){width="672"}

``` r
data.model <- subset(data, ,-c(customerID, gender,PhoneService, MultipleLines, TotalCharges))
```
:::

::: {#decision-tree .section .level2}
## Decision Tree

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/653803f7758f3149e4626ad2a0b32cd7923196d0.png){width="672"}

    ## Confusion Matrix and Statistics
    ## 
    ##           Reference
    ## Prediction  No Yes
    ##        No  942 199
    ##        Yes  90 174
    ##                                           
    ##                Accuracy : 0.7943          
    ##                  95% CI : (0.7722, 0.8152)
    ##     No Information Rate : 0.7345          
    ##     P-Value [Acc > NIR] : 1.131e-07       
    ##                                           
    ##                   Kappa : 0.4183          
    ##                                           
    ##  Mcnemar's Test P-Value : 2.112e-10       
    ##                                           
    ##             Sensitivity : 0.9128          
    ##             Specificity : 0.4665          
    ##          Pos Pred Value : 0.8256          
    ##          Neg Pred Value : 0.6591          
    ##              Prevalence : 0.7345          
    ##          Detection Rate : 0.6705          
    ##    Detection Prevalence : 0.8121          
    ##       Balanced Accuracy : 0.6896          
    ##                                           
    ##        'Positive' Class : No              
    ## 

    ## Setting levels: control = 0, case = 1

    ## Setting direction: controls < cases

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/794d54212c7aa8cccf7a3d8f20f7a651b7a8b766.png){width="672"}

> ACC is 0.811

::: {#tree-pruning .section .level3}
### tree pruning

    ## 
    ## Classification tree:
    ## rpart(formula = Churn ~ ., data = train, method = "class")
    ## 
    ## Variables actually used in tree construction:
    ## [1] Contract        InternetService TechSupport     tenure         
    ## 
    ## Root node error: 1496/5627 = 0.26586
    ## 
    ## n= 5627 
    ## 
    ##         CP nsplit rel error  xerror     xstd
    ## 1 0.069742      0   1.00000 1.00000 0.022153
    ## 2 0.013703      3   0.79078 0.81751 0.020681
    ## 3 0.010000      5   0.76337 0.80816 0.020595

    ## [1] 0.01

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/653803f7758f3149e4626ad2a0b32cd7923196d0.png){width="672"}
:::
:::

::: {#random-forest .section .level2}
## Random FOrest

::: {#reprocessing-1 .section .level3}
### Reprocessing

> Change No phone service at MultipleLines columns to no.

> Change SeniorCitizen, 0 - No, 1 -Yes

> Remove some highly correlated input attributes that affect the
> analysis.
:::

::: {#model-1 .section .level3}
### 2.2.2 Model

> Training by random forest.

    ## 
    ## Call:
    ##  randomForest(formula = Churn ~ ., data = training) 
    ##                Type of random forest: classification
    ##                      Number of trees: 500
    ## No. of variables tried at each split: 4
    ## 
    ##         OOB estimate of  error rate: 22.43%
    ## Confusion matrix:
    ##       No Yes class.error
    ## No  3385 488   0.1260005
    ## Yes  695 707   0.4957204

> accuracy on train data.

    ## Confusion Matrix and Statistics
    ## 
    ##           Reference
    ## Prediction   No  Yes
    ##        No  3636  233
    ##        Yes  237 1169
    ##                                           
    ##                Accuracy : 0.9109          
    ##                  95% CI : (0.9029, 0.9185)
    ##     No Information Rate : 0.7342          
    ##     P-Value [Acc > NIR] : <2e-16          
    ##                                           
    ##                   Kappa : 0.7719          
    ##                                           
    ##  Mcnemar's Test P-Value : 0.8899          
    ##                                           
    ##             Sensitivity : 0.9388          
    ##             Specificity : 0.8338          
    ##          Pos Pred Value : 0.9398          
    ##          Neg Pred Value : 0.8314          
    ##              Prevalence : 0.7342          
    ##          Detection Rate : 0.6893          
    ##    Detection Prevalence : 0.7335          
    ##       Balanced Accuracy : 0.8863          
    ##                                           
    ##        'Positive' Class : No              
    ## 

> draw AUC

    ## Setting levels: control = 0, case = 1

    ## Warning in value[[3L]](cond): Ordered predictor converted to numeric vector.
    ## Threshold values will not correspond to values in predictor.

    ## Setting direction: controls < cases

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/7b12492068da93ea32bfcb45aa52130893f45844.png){width="672"}

    ## mtry = 4  OOB error = 22.98% 
    ## Searching left ...
    ## mtry = 8     OOB error = 23.64% 
    ## -0.02887789 0.05 
    ## Searching right ...
    ## mtry = 2     OOB error = 21.78% 
    ## 0.0519802 0.05 
    ## mtry = 1     OOB error = 24.28% 
    ## -0.1148825 0.05

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/6ecb652c9f049e2b457c9379394e93b62ab28262.png){width="672"}

> improve model wit ntree=200, mtry=2 on train.

    ## 
    ## Call:
    ##  randomForest(formula = Churn ~ ., data = training, ntree = 200,      mtry = 2, importance = TRUE, proximity = TRUE) 
    ##                Type of random forest: classification
    ##                      Number of trees: 200
    ## No. of variables tried at each split: 2
    ## 
    ##         OOB estimate of  error rate: 22.14%
    ## Confusion matrix:
    ##       No Yes class.error
    ## No  3469 404   0.1043119
    ## Yes  764 638   0.5449358

> test and retrain.

    ## Confusion Matrix and Statistics
    ## 
    ##           Reference
    ## Prediction   No  Yes
    ##        No  1163  252
    ##        Yes  127  215
    ##                                           
    ##                Accuracy : 0.7843          
    ##                  95% CI : (0.7643, 0.8033)
    ##     No Information Rate : 0.7342          
    ##     P-Value [Acc > NIR] : 6.973e-07       
    ##                                           
    ##                   Kappa : 0.3957          
    ##                                           
    ##  Mcnemar's Test P-Value : 1.897e-10       
    ##                                           
    ##             Sensitivity : 0.9016          
    ##             Specificity : 0.4604          
    ##          Pos Pred Value : 0.8219          
    ##          Neg Pred Value : 0.6287          
    ##              Prevalence : 0.7342          
    ##          Detection Rate : 0.6619          
    ##    Detection Prevalence : 0.8054          
    ##       Balanced Accuracy : 0.6810          
    ##                                           
    ##        'Positive' Class : No              
    ## 

> draw AUC on test data.

    ## Setting levels: control = 0, case = 1

    ## Warning in value[[3L]](cond): Ordered predictor converted to numeric vector.
    ## Threshold values will not correspond to values in predictor.

    ## Setting direction: controls < cases

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/90799cf5a2527bfeb73a83b1fc307903bd5a1928.png){width="672"}

> Top 10 feature importance

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/dc4bf6c2ec831c3d74704f41d6dce91a15832f62.png){width="672"}
:::
:::

::: {#thuật-toán-knn .section .level2}
## 2.3 Thuật toán KNN

::: {#tiền-xư-lí-dữ-liệu .section .level3}
### 2.3.1 Tiền xư lí dữ liệu

> Remove customerId \*\*

> Remove null data

    ##           gender    SeniorCitizen          Partner       Dependents 
    ##                0                0                0                0 
    ##           tenure     PhoneService    MultipleLines  InternetService 
    ##                0                0                0                0 
    ##   OnlineSecurity     OnlineBackup DeviceProtection      TechSupport 
    ##                0                0                0                0 
    ##      StreamingTV  StreamingMovies         Contract PaperlessBilling 
    ##                0                0                0                0 
    ##    PaymentMethod   MonthlyCharges     TotalCharges            Churn 
    ##                0                0                0                0

    ## 'data.frame':    7032 obs. of  20 variables:
    ##  $ gender          : chr  "Female" "Male" "Male" "Male" ...
    ##  $ SeniorCitizen   : int  0 0 0 0 0 0 0 0 0 0 ...
    ##  $ Partner         : chr  "Yes" "No" "No" "No" ...
    ##  $ Dependents      : chr  "No" "No" "No" "No" ...
    ##  $ tenure          : int  1 34 2 45 2 8 22 10 28 62 ...
    ##  $ PhoneService    : chr  "No" "Yes" "Yes" "No" ...
    ##  $ MultipleLines   : chr  "No phone service" "No" "No" "No phone service" ...
    ##  $ InternetService : chr  "DSL" "DSL" "DSL" "DSL" ...
    ##  $ OnlineSecurity  : chr  "No" "Yes" "Yes" "Yes" ...
    ##  $ OnlineBackup    : chr  "Yes" "No" "Yes" "No" ...
    ##  $ DeviceProtection: chr  "No" "Yes" "No" "Yes" ...
    ##  $ TechSupport     : chr  "No" "No" "No" "Yes" ...
    ##  $ StreamingTV     : chr  "No" "No" "No" "No" ...
    ##  $ StreamingMovies : chr  "No" "No" "No" "No" ...
    ##  $ Contract        : chr  "Month-to-month" "One year" "Month-to-month" "One year" ...
    ##  $ PaperlessBilling: chr  "Yes" "No" "Yes" "No" ...
    ##  $ PaymentMethod   : chr  "Electronic check" "Mailed check" "Mailed check" "Bank transfer (automatic)" ...
    ##  $ MonthlyCharges  : num  29.9 57 53.9 42.3 70.7 ...
    ##  $ TotalCharges    : num  29.9 1889.5 108.2 1840.8 151.7 ...
    ##  $ Churn           : chr  "No" "No" "Yes" "No" ...
    ##  - attr(*, "na.action")= 'omit' Named int [1:11] 489 754 937 1083 1341 3332 3827 4381 5219 6671 ...
    ##   ..- attr(*, "names")= chr [1:11] "489" "754" "937" "1083" ...

> accuracy function

``` r
cost_matrix <- matrix(c(1,0,0,1), nrow = 2)
cost_matrix
```

    ##      [,1] [,2]
    ## [1,]    1    0
    ## [2,]    0    1

``` r
accuracy <- function(cm){
  return(cm*cost_matrix)
}
```

> cross validation with 7 fole
:::

::: {#model-2 .section .level3}
### 2.3.2 Model

> create a matrix save result for each k

    ## [1] 5625

    ## [1] 5625

> train data and save result with k from 1 to 100

> draw chart result by k

    ## Warning in geom_line(colour = "red", linetype = "dashed", fill = "white"):
    ## Ignoring unknown parameters: `fill`

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/9e0cc1e70520c524e3ce0c853bb1fc2107ac985e.png){width="672"}

> Find the best k

    ## [1] 62

> Predict with test data

> accuracy

    ## [1] 0.7867804

> AUC

    ## Setting levels: control = 0, case = 1

    ## Setting direction: controls < cases

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/5778899745fdb2b0f6b82de88d234e402041b12b.png){width="672"}
:::
:::

::: {#logistic-regression .section .level2}
## 2.4 Logistic Regression

::: {#reprocessing-2 .section .level3}
### 2.3.1 Reprocessing

> Tranform tenure to 5 level "1-2 years", "2-3 years", "3-4 years", "4-5
> years", "5-6 years"

    ## 
    ##  0-1 year 1-2 years 2-3 years 3-4 years 4-5 years 5-6 years 
    ##      2186      1024       832       762       832      1407

> transform data class to (0, 1)

> Remove CustomerID and create fake variabel.

> Remove rows has "No phone service"
:::

::: {#model-3 .section .level3}
### 2.4.2 Model

> Cross Validation (Confusion Matrix & ROC)

> Train set

    ## Confusion Matrix and Statistics
    ## 
    ##           Reference
    ## Prediction   No  Yes
    ##        No  3501  726
    ##        Yes  342  665
    ##                                           
    ##                Accuracy : 0.7959          
    ##                  95% CI : (0.7848, 0.8068)
    ##     No Information Rate : 0.7342          
    ##     P-Value [Acc > NIR] : < 2.2e-16       
    ##                                           
    ##                   Kappa : 0.4267          
    ##                                           
    ##  Mcnemar's Test P-Value : < 2.2e-16       
    ##                                           
    ##             Sensitivity : 0.9110          
    ##             Specificity : 0.4781          
    ##          Pos Pred Value : 0.8282          
    ##          Neg Pred Value : 0.6604          
    ##              Prevalence : 0.7342          
    ##          Detection Rate : 0.6689          
    ##    Detection Prevalence : 0.8076          
    ##       Balanced Accuracy : 0.6945          
    ##                                           
    ##        'Positive' Class : No              
    ## 

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/bc28a1b98fa4e7d9dd59d4d98b0a23febd1413f3.png){width="672"}

> Test set

    ## Confusion Matrix and Statistics
    ## 
    ##           Reference
    ## Prediction   No  Yes
    ##        No  1216  250
    ##        Yes  115  228
    ##                                          
    ##                Accuracy : 0.7982         
    ##                  95% CI : (0.779, 0.8165)
    ##     No Information Rate : 0.7358         
    ##     P-Value [Acc > NIR] : 3.474e-10      
    ##                                          
    ##                   Kappa : 0.4295         
    ##                                          
    ##  Mcnemar's Test P-Value : 2.318e-12      
    ##                                          
    ##             Sensitivity : 0.9136         
    ##             Specificity : 0.4770         
    ##          Pos Pred Value : 0.8295         
    ##          Neg Pred Value : 0.6647         
    ##              Prevalence : 0.7358         
    ##          Detection Rate : 0.6722         
    ##    Detection Prevalence : 0.8104         
    ##       Balanced Accuracy : 0.6953         
    ##                                          
    ##        'Positive' Class : No             
    ## 

![](vertopal_13072b7bdc7249c89d6eab327256fbc8/b153fb000efbd881a3df58143dc2832c116d91eb.png){width="672"}
:::
:::
:::
:::
