************************
Setup Karan
************************

Setup   Karan    (required   for   windows   automation)
- For windows automation using calm to work, a separate windows server(2012) has to be setup and karan.exe(binary) has to be installed on the server (setup instructions will be there in the guide)
- Once   the   karan   is   configured,   the   end   user   machines(vms)   that   you   want   to   provision   using   calm   *do not   require   karan   to   be   installed   on   them   *.   The   end   user   images   must   have   ps   remoting   enabled(which will   be   documented   and   by   default   enabled   on   2012/2016   servers)   .
- Additionally,   if   there   is   requirement   for   lot   of   windows   automation   flows/apps,   you   can   create multiple   vms   with   karan   installed   and   configure   it   to   work   with   existing   calm   vm.

**NOTE:** 

This   section   is   not   applicable   to   external   users/customers,   since   we   cannot   distribute   a Windows   image   externally.   For   external   users/customers   please   check  t   his .
1. Stop   firewall   on   PC   (Required   for   EA2)   -    sudo   service   iptables   stop
2. Upload   the   qcow2    image    to   the   required   nutanix   cluster   through   image   configuration   in   prism   UI
3. Provision   the   karan   machine   using   the   uploaded   image   by   attaching   a   disk   to   the   vm.
4. Credentials   -
a. Username   -      administrator
b. Password   -   nutanix/4u
5. Power   on   the   vm   and   go   to   console   and   run   the   Karan_Config.ps1   script   in   desktop   with
powershell.   (Input   parameter   is   the   PC_IP/CALM_IP).
