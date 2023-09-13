```.py
class OSIModel:
    def __init__(self, msg):
        self.msg = msg
    def transmit(self):
        for i in self.msg:
            num = ord(i)
            bin = self.to_bin(num)
            return bin
    def to_bin(self, num):
        bin = ""
        while num>0:
            res = num%2
            bin = f"{res}"+bin
            num = num//2
        while len(bin)<8:
            bin = "0"+bin
            bin = "0"+bin
        return bin
```
![IMG_3971](https://github.com/idrlykforeal/year_2/assets/100017195/45d78bdc-a72f-4821-8c61-0eb26f117aa9)
