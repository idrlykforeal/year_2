```.py
def CheckCorrect(information):
    i_1 = information[0:len(information)//3]
    i_2 = information[len(information)//3:2*len(information)//3]
    i_3 = information[2*len(information)//3:]
    
    
    for i in range(len(i_1)):
        error = True
        if i_1[i] == i_2[i] or i_1[i] == i_3[i]:
            error = False
            break
        elif i_2[i] == i_3[i]:
            i_1[i] = i_2[i]
        elif i_1[i]==i_2[i]:
            i_3[i] = i_1[i]
        elif i_1[i]==i_3[i]:
            i_2[i] = i_1[i]
        return error, i_1+i_2+i_3
            
```
![IMG_3972](https://github.com/idrlykforeal/year_2/assets/100017195/7279776d-7773-4980-bf5b-cab85e96b71a)
