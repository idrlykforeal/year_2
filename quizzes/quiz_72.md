# code for mac generator machine

code:

```.py
import random

class MACGenerator:
    def __init__(self):
        self.hex_dict = {
            10: 'A',
            11: 'B',
            12: 'C',
            13: 'D',
            14: 'E',
            15: 'F'
        }
    def int_to_hex(self, dec:int):
        if dec<=9:
            return f"{dec}"
        else:
            return self.hex_dict[dec]
    def random_hex(self):
        hex=self.int_to_hex(random.randint(0, 15))
        return hex
    def mac_generator(self, N: int):
        addresses = []
        while len(addresses) < N:
            add= ""
            for j in range(6):
                for k in range(2):
                    add += self.random_hex()
                add += ":"
            if add not in addresses:
                addresses.append(add[:-1])
        return addresses

if __name__ == '__main__':
    mac = MACGenerator()
    print(mac.mac_generator(20))
```
