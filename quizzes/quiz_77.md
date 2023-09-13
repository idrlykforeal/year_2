```.py
# parity checker

class ParityChecker:
    def __init__(self, in_str):
        self.in_str = in_str

   def check(self):
        count_1 = 0
        for i in self.in_str:
            if i == "1":
                count_1 += 1
            result = not count_1%2
            correct= (result == self.in_str[1])
            return correct
```
![IMG_3973](https://github.com/idrlykforeal/year_2/assets/100017195/864fb50b-74fe-4b97-aa5b-92585bdfcea9)
