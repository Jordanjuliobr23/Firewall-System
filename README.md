# Firewall-System---Open-Systems-Advanced-Administration 🚫

# 📋 About the project:
This is a academy project from discipline Open Systems Advanced Administration. 
 The objective of project is buildin a network topology with the Server and Client programs
 Network Protocols and Tecnologies: Iptables, NTP, Rsyslog 
         
# 🛜 Network Settings: 
    └── 📌 Net Strap: 192.168.56.x
    
    └── 🔥Firewall/Network : 
          └── Network Interface 1: 
              └── IP-Address: DHCP (Automatic Address)
              └── Connection: NAT

          └── Network Interface 2: 
              └── IP-Address: 192.168.56.1/24
              └── Connection: Internal Network 

      └── 📑 Client/Internal Server: 
          └── Network Interface 1: 
              └── IP-Address: 192.168.56.10/24
              └── Connection: Internal Network
              └── Gateway: 192.168.56.1/24

       

              
        
# 🌲Topology:
 
    └── 🔥 Firewall/Gateway: 

              ✅ Enable Datagram Route: 
                        sudo sysctl -w net.ipv4.ip_forward=1

                🔒 Politics IP-Tables: 
                      └── IP-Forwarding enable
                      └── Stateful Inspection enable 
                      └── SSH connections enable
                      └── Standart Politic: Drop 
                      └── Nat connection from network where are the client
                      └── Enable only traffic forwarding coming from the client's network
                      
                  🌍 NTP Setings: 
                         └── NTP protocoll install
                         └── Connect host clock with NTP.br servers

                  💾 Rsyslog:
                       └── Rsyslog install
                        └── Send all LOGs from internal service 


    └──  💻 Client/Internal Service: 

              🌐 Enable Internet Access 
              
              💾 Rsyslog Server:     
                    └── Run a Syslog server
                    └── Receive and guard Gateway LOGs

      
                  


      
