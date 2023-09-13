```.py
# layer 4 firewall

class Firewall:
    def __init__(self, data):
        self.data = data

    def to_dec(self, bin):
        dec = 0
        for i in range(len(bin)):
            dec += bin[15-i] * (2**i)
        return dec

    def filter(self):
        port = self.data[:16]
        error = "Filtered"
        msg = None

        if self.to_dec(port) == 80 or self.to_dec(port) == 22123:
            error = "Allowed"
            msg = self.data[16:]

        return error, msg
```

![IMG_3974](https://github.com/idrlykforeal/year_2/assets/100017195/d44da99b-217b-409b-9872-06674d3c62cf)
