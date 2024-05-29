enable
    configure terminal
    !configurações da VYT   

        Line vty 0 4
        Login local
        password 123@senac
        logging synchronous
        exec-timeout 5 30
        transport input ssh
        end
        write

enable
    configure terminal
    ip default-gateway 192.168.1.254
    interface vlan 1
    description interface SVI do sw-01
    ip address 192.168.1.250 255.255.255.0
    no shutdown
    end
    write

SSH - OpenSSH
enable
    configure terminal 
    crypto key generate rsa general-keys modulus 1024

    Ip ssh version 2
    Ip ssh time-out 60]
    Ip ssh authentication-retries-2
