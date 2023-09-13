# ipv6 generator

code:

```.py
import random
import time

class ipv6Machine:
    def __init__(self):
        self.hex_dict = {
            10: 'A',
            11: 'B',
            12: 'C',
            13: 'D',
            14: 'E',
            15: 'F'
        }

    def dec_to_hex(self, dec:int):
        if dec<=9:
            return f"{dec}"
        else:
            return self.hex_dict[dec]

    def random_hex(self):
        hex=self.dec_to_hex(random.randint(0, 15))
        return hex

    def ipv6machine(self, N: int):
        output_list = []
        while len(output_list) < N:
            ip_add = ''
            for digit in range(8):
                for j in range(4):
                    ip_add += self.random_hex()
                ip_add += ':'
            if ip_add not in output_list:
                output_list.append(ip_add[:-1])
        return output_list

if __name__ == '__main__':
    start_time = time.time()
    ipv6 = ipv6Machine()
    addresses= ipv6.ipv6machine(10000)
    end_time = time.time()

    execution_time = end_time - start_time

    print(f"Execution time: {execution_time:.6f} seconds")
```
![IMG_3968](https://github.com/idrlykforeal/year_2/assets/100017195/c9ac91fa-83d0-4a5f-9dea-90233734aeee)
