code:
```.py
def ipv4machine():
    a,b,c,d = 0,0,0,0
    ip_add=[]
    for ip in range(256*4):
        a = ip%256
        b = (ip//256)%256
        c = (ip//(256**2))%256
        d = (ip//(256**3))%256
        ip_add.append(f"{d}.{c}.{b}.{a}")
    return ip_add
```
![IMG_3967](https://github.com/idrlykforeal/year_2/assets/100017195/3fd3bf1e-8e60-4e23-abce-02162602d867)
