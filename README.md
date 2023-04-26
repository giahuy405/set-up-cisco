
## Định tuyến OSPF 
| ![space-1.jpg](https://lh4.googleusercontent.com/YVPv0035N2JlKXe2vC6p_BzSna3rCmbeIRnAqjxOTnlAKkHBCZQ-YnhlUnCDeYQGFGzdUaWQN9aHT98=w2476-h1214) | 
|:--:| 
| *Sơ đồ* |
```
R1(config)#router OSPF 1 
R1(conffig-router)#network 131.108.1.0 0.0.0.255 area 0 
R1(conffig-router)#network 131.108.3.0 0.0.0.255 area 0
// remember to exit and type 'yes' then Enter to configure
R1#clear ip ospf process
```
Show bg định tuyến
```
R2#show ip route ospf
```

- Có [110/65] -> `AD=110` và `Metric=65`
```
R1#show ip ospf neighbor   // show ip của thằng đối diện
R1#show ip ospf           
```

Hiệu chỉnh router ID 
```
R1(config)#router ospf 1
R1(config-router)#router-id 1.1.1.1   // đề kêu gì ghi ip đó
R1#show ip route ospf
R1#clear ip ospf process   // nhớ clear để làm mới lại 
```

