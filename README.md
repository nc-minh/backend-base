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