# Backend-Engineer---Base

## OSI model
- send out:
```
Layer 7 Application: Get/10.0.0.3 80, HTTP Header, Cookies, Content-Type,...
```
```
Layer 6 Presentation: Encrypt if necessary (https)
```
```
Layer 5 Session: Establish session tag it
```
```
Layer 4 Transport: break into segment, add ports/seq
```
```
Layer 3 Network: get into segment in Layer 4 and add to destination ip (use dns)
```
```
Layer 2 Data Link: get MAC address (use ARP) and add to segment
```
```
Layer 1 Physical: convert segment -> bit (01) and transport ->>>>
```
->> When the signal is sent, all computers in the network can catch the packet you send

- receive:
```
Layer 1 Physical: receive bit in the networks
```
```
Layer 2 Data Link: convert bit -> segment if same MAC address
```
```
Layer 3 Network: get ip address in segment and compare with your device 
```
```
Layer 4 Transport: Verify port/seq resend error packets
```
```
Layer 5: Session: Collect session ID order
```
```
Layer 6 Presentation: Decrypt if necessary (HTTPS)
```
```
Layer 7 Application: Get/10.0.0.3.80 - HTTP Header, Cookies, Content-Type,...
```

## TCP - Transmission Control Protocol
- Layer 7 Application: HTTP ver1.0 ver1.1 ver2.0 ver3.0(QUIC)
- Layer 4 Transport: TCP

- TCP transport needs to make a connection use (Three-way handshake)
    (Advantages)
    + Acknowledgement : cơ chế báo nhận
    + Guaranteed Delivery : đảm bảo tin cậy
    + Recovery : khôi phục
    + Ordered Package : trật tự các gói tin (khi có nhiều gói tin)
    + Flow Control : kiểm soát luồng
    + Congestion: kiểm soát tắc nghẽn
    + Pipeline : kiểu truyền Pipeline (cùng lúc nhận và cùng lúc thông báo)
    (Defect)
    + Larger Package : gói tin lớn
    + More Bandwidth : tốn băng thông
    + Slower than UDP : chậm hơn UDP
    + Stateful : có trạng thái (khi một trong 2 thiết bị mất kết nối phải làm lại từ đầu)

    (use TCP with)
    HTTP SSH FTP(truyền file) Telnet SMTP IMAP/POP

## UDP - User Datagram Protocol