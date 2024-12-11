# SecurityFocusOnline CTF本地端開啟

- 開啟vitualbox選擇最底下的虛擬機並點選啟動虛擬機

## 輸入帳號密碼
```
ksu
Ksu@09====
```


## 查看IP地址
```
ip addr | grep 192.168
```


## 使用Xshell連線進虛擬機
```
192.168.x.xxx
```

## 輸入帳號密碼

```
ksu
Ksu@0956327000
```
## 成功登入

## 使用root最高權限運行docker_start.sh(要多打2次以上確保docker都已開啟)
```
sudo sh docker_start.sh
```



## 檢查題目docker狀態
```
sudo docker ps -a
```


## 開LINUX101的ssh連線
```
sudo docker exec -ti 8e8390f5604f bash 
```
```
sh /bin/start.sh;exit;
```

## 開LINUX102的ssh連線

```
sudo docker exec -ti 95c8eec123b9 bash 
```
```
sh /bin/start.sh;exit;
```


## 連線ctfd網頁端-確認網頁正常開啟

- 開啟網頁後,點擊導覽列最右邊的login並輸入平台管理員帳號
```
ksu
Ksu@0956327000
```

- 點擊導覽列的Chellanges進入查看題目是否都正常顯示
- 完成開啟
