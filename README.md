vcx
===

vcx is a vircurex live ticker that gives you the current statistics of crypto currencies


Prerequisites:
--------------

In order to run this script your need the following Perl modules installed:

LWP::UserAgent
XML::Simple
LWP::UserAgent::Protocol::https

If you have ArchLinux running, just install everything with this command:


    sudo pacman -S perl-lwp-protocol-https perl-xml-simple perl-libwww


This script is very minimalistic and doesn't take commandline arguments. Please
edit the script itself and set the @watchlist to whatever you need. For example,
if you want to see DOGE and LTC stats:

    my @watchlist = qw(DOGE LTC);



Sample output should look similar to this (depending on your watchlist):

    18.01.2014 - 17:49:14 - refresh approx. every 5 seconds (+/- some seconds for network latency and server load)
    HB - highest bid / LA - lowest ask / LT - last executed trade / VOL_BTC - Trading Volume in BTC
    TENDENCY is a percentual value and will appear after some time, please be patient :)
    Tendency calculates like this: (last_trade / average_of_20_or_50_last_recorded_trades * 100) - 100
    PLEASE BE AWARE THAT THE API IS NOT UPDATED AS FAST AS WE POLL!

     CUR  :          HB  :          LA  :          LT  :     VOL_BTC  :     TEND_20  :     TEND_50  :    TEND_200


     ANC  :  0.00471000  :  0.00479965  :  0.00471000  :  0001.97691  :  -0.0000000  :    % 

     DGC  :  0.00038300  :  0.00040000  :  0.00039500  :  0000.75585  :  -0.0000000  :    % 

    DOGE  :  0.00000066  :  0.00000067  :  0.00000066  :  0157.37374  :  +4.4303797  :    % 

     DVC  :  0.00000045  :  0.00000047  :  0.00000046  :  0005.42896  :  +0.0000000  :    % 

     FTC  :  0.00036751  :  0.00037999  :  0.00036751  :  0001.05901  :  +0.0000000  :    % 

     LTC  :  0.02870144  :  0.02899106  :  0.02899106  :  0032.47034  :  -0.0000000  :    % 

     PPC  :  0.00692000  :  0.00704765  :  0.00687000  :  0009.19562  :  +0.0000000  :    % 

     QRK  :  0.00007949  :  0.00008339  :  0.00007948  :  0000.79859  :  -0.0000000  :    % 

     TRC  :  0.00053000  :  0.00054729  :  0.00053000  :  0000.44908  :  +0.0000000  :    % 

     WDC  :  0.00042700  :  0.00042701  :  0.00042701  :  0035.98302  :  -0.0000000  :    % 

     XPM  :  0.00380006  :  0.00398994  :  0.00382099  :  0001.65990  :  +0.0000000  :    % 



Have fun!
