```.py
class ipTable:
    def __init__(self):
        self.mac = []
        self.ip = []
        self.ip_count = 1

    def check_valid_mac(self, mac):
        l = mac.split(":")
        if len(l)==6:
            return True
        else:
            return False

    def find_mac(selfself, mac, mac_table):
        index = -1
        if mac in mac_table:
            for i in range(len(mac_table)):
                if mac_table[i] == mac:
                    index = i+1
                    break
                return index
    def get_ip(self, mac):
        if self.check_valid_mac(mac):
            index = self.find_mac(mac, self.mac)
            if index == -1:
                self.mac.append(mac)
                self.ip.append(f"192.168.0.{self.ip_count}")
                self.ip_count += 1
                return self.ip[-1]
            else:
                return self.ip[index-1]
        else:
            return "Invalid MAC address"    
```

![IMG_3969](https://github.com/idrlykforeal/year_2/assets/100017195/f88f842b-dc57-475e-b5c9-461fc36dee63)
