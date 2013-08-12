Linux_hosts_update
==================

A bash script for update Hosts.

#Function
    Get a hosts file from the specified url, then replace /etc/hosts.
    Generate a hosts file by nslookp with a DNS server.

#Usage
    update_hosts DNS-server  //DNS-server: --generate Hosts by nslookup
                             //if '-1' --get Hosts from $dns_download_url
    You can change the url by variable:'dns_download_url' in update_hosts script. 
    default it set dns_download_url="https://smarthosts.googlecode.com/svn/trunk/hosts"
    also you can add the the hostname in scripte bellow line "----hosts_list----"

#Example:
    eg: 1) Use goolge public DNS server to generate a hosts file.
           command: ./update_hosts 8.8.8.8 |tee /tmp/hosts
                    mv /tmp/hosts /etc/hosts
        2) Get host from a specified url.
           command ./update_hosts -1


