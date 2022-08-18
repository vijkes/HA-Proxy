frontend mylb1
        bind *:81
        mode http
        timeout client 10s
        option forwardfor
        default_backend myhttp_backend_leastconn

frontend mylb2
        bind *:82
        mode http
        default_backend myhttp_backend
        timeout client 10s

frontend mylb3
        bind *:8080
        stats enable
#       stats refresh 5s
        stats uri /stats
        mode http
        stats auth admin:redhat1
        timeout client 10s


backend myhttp_backend
#       balance roundrobin
#       balance static-rr
        balance source
        mode http
        timeout connect 5s
        timeout server 100s
        server server1 3.22.101.10:80   weight 1 maxconn 1 check
        server server2 18.220.192.196:80 weight 1 maxconn 1 check
        server server3 18.190.157.172:80 weight 1 maxconn 1 check


backend myhttp_backend_leastconn
        balance leastconn
        mode http
        timeout connect 5s
        timeout server 125s
        server server1 3.22.101.10:80   weight 1 maxconn 789 check
        server server2 18.220.192.196:80 weight 1 maxconn 456 check
        server server3 18.190.157.172:80 weight 4 maxconn 551 check
