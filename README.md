# TTGO-7000G
Testing TTGO -T-Call with SIM 7000G
* 
* I had a hard time get this to work. Information etc hare on various githubs
* https://github.com/vshymanskyy/TinyGSM/issues/448
* 
*  The sequence below finally helped ... i worked for Twilio,holgram and bell 
*  
*  mvk@ca.ibm.com / markus@vankempen.org - 2021-Apr-06
*  
*  
//Set the APN for the wireless connection. Please check the APN for your network
AT+CSTT="super" // twilio super SIM
WAIT=1
//Bring up Connection...
AT+CIICR
WAIT=3
//Get the local IP address
AT+CIFSR
WAIT=2
//Get the GNSS location information
AT+CIPPING="www.google.com"
