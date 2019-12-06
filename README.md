# GFW-ladder
ladder

# FOR google cloud 
1、register google cloud Account and set up VM instance 
  region and zone
  machine OS : cenOS
  allow http and https
  select security to add SSH key from XShell or not 
  
    (for XShell to connect VPS.if not ,we must connect VPS by SSH of browser.
    key can be created and added after instance created.)
    
2、test ip ping ,port and route
  http://tool.chinaz.com/port/ (port 22 allowed)
  https://tools.ipip.net/traceroute.php (ping < 50 ms)
  
3、set up Departure and Inbound services

  VPC -> Firewall rules -> create new : all allowed and IP scope:0.0.0.0/0
  
  modifying instance for SSH key : add ssh-rsa and username at the end
  
  modifying instance for Firewall : add internet label (Firewall rules you created)
  
4、deploy v2ray for ss

  ssh :
  
    bash <(curl -s -L https://git.io/v2ray.sh) 
    
    systemctl stop firewalld && systemctl disable firewalld (or not)
    
    v2ray ssqr (for ss)
    
5、configuration in pc or mobile

  add configuration in VPC and v2ray
  
6、to find our way
  
 
