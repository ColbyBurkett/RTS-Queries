# Networking - Flow

## **Connections by Dest Port 53**

```sql
NetworkFlow status, proto, direction, src_ip, src_port, dst_ip, dst_port
    WHERE NetworkFlow dst_port equals "53"
```


## **Connections by OSI Protocol - SINGLE**

```sql
NetworkFlow status, proto, direction, src_ip, src_port, dst_ip, dst_port
    WHERE NetworkFlow dst_port equals "53"
        AND NetworkFlow proto equals "tcp"
```

## **Connections by OSI Protocol - MANY**

```sql
NetworkFlow status, proto, direction, src_ip, src_port, dst_ip, dst_port
    WHERE NetworkFlow dst_port equals "53"
        AND NetworkFlow proto equals "tcp"
            OR NetworkFlow proto equals "udp"
```


## **Connections by Dest Port Number - SINGLE**

```sql
NetworkFlow status, proto, direction, src_ip, src_port, dst_ip, dst_port
    WHERE NetworkFlow dst_port equals "53"
```

## **Connections by Dest Port Number - MANY**

```sql
NetworkFlow status, proto, direction, src_ip, src_port, dst_ip, dst_port
    WHERE NetworkFlow dst_port equals "53"
        OR NetworkFlow dst_port equals "443"
        OR NetworkFlow dst_port equals "80"
```


## **Connections by Dest IP and Dest Port 53 - SINGLE**

```sql
NetworkFlow status, proto, direction, src_ip, src_port, dst_ip, dst_port
    WHERE NetworkFlow dst_port equals "53"
        AND NetworkFlow dst_ip equals "10.0.0.1"
```

## **Connections by Dest IP and Dest Port 53 - MANY**

```sql
NetworkFlow status, proto, direction, src_ip, src_port, dst_ip, dst_port
    WHERE NetworkFlow dst_port equals "53"
        AND NetworkFlow dst_ip equals "10.0.0.1"
            OR NetworkFlow dst_ip equals "10.0.0.2"
            OR NetworkFlow dst_ip equals "10.0.0.3"
```
