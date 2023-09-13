```.py
class DataPackage:
    def __init__ (self, max_rx, ip_rx, mac_sx, ip_sx, data):
        self.max_rx = max_rx
        self.ip_rx = ip_rx
        self.mac_sx = mac_sx
        self.ip_sx = ip_sx
        self.data = data
        self.header = f"{self.max_rx}:{self.ip_rx}:{self.mac_sx}:{self.ip_sx}"
    def split_data(self,data)->list:
        str = ""
        out = []
        for i in range(len(data)):
            if len(str) ==4:
                out.append(str)
                str = ""
            str += data[i]
        out.append(str)
        return out
    def build_package(self):
        pkgs = []
        for i in self.split_data(self.data):
            pkgs.append(f"{self.header}:{i}")
        return pkgs
```

![IMG_3970](https://github.com/idrlykforeal/year_2/assets/100017195/49807120-477e-4d84-9c04-f85d2dfa4b40)
