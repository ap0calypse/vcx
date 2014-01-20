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
if you want to see only DOGE and LTC stats:

    my @watchlist = qw(DOGE LTC);



Sample output should look similar to this (depending on your watchlist):

     20.01.2014 - 00:02:13 - refresh approx. every 2-3 seconds (+ some seconds [network/load]) [ 000000509 polls ]
     HB - highest bid / LA - lowest ask / LT - last executed trade / VOL_BTC - Trading Volume in BTC
     TENDENCY is a percentual value and will appear after some time, please be patient :)
     Tendency calculates like this: (last_trade / average_of_x_recorded_trades * 100) - 100

     CUR  :          HB  :          LA  :          LT  :     VOL_BTC  :     TEND_50  :    TEND_250  :    TEND_500


     ANC  :  0.00432100  :  0.00451998  :  0.00451998  :  0003.76182  :  -000.00000  :  +000.00000  :  +000.00000  % 

     DGC  :  0.00036000  :  0.00036100  :  0.00036000  :  0001.36749  :  +000.00000  :  +000.00000  :  +000.00000  % 

    DOGE  :  0.00000080  :  0.00000082  :  0.00000081  :  0167.20850  :  +000.02470  :  +002.16437  :  +001.36911  % 

     DVC  :  0.00000063  :  0.00000065  :  0.00000065  :  0023.13515  :  +000.00000  :  -000.28228  :  +001.13269  % 

     FRC  :  0.00005850  :  0.00006599  :  0.00005850  :  0000.96631  :  +000.00000  :  +000.00000  :  +000.00000  % 

     FTC  :  0.00036900  :  0.00037001  :  0.00036900  :  0000.46527  :  -000.00000  :  +000.00000  :  -000.00985  % 

     I0C  :  0.00002401  :  0.00002491  :  0.00002517  :  0004.35762  :  +000.00000  :  +000.00000  :  +000.00000  % 

     IXC  :  0.00013501  :  0.00014848  :  0.00014848  :  0002.05911  :  -000.00000  :  +000.00000  :  +004.16082  % 

     LTC  :  0.02900005  :  0.02919999  :  0.02900001  :  0009.44133  :  -000.00000  :  +000.00000  :  -000.37505  % 

     NMC  :  0.00711001  :  0.00737598  :  0.00711001  :  0005.80971  :  +000.00000  :  +000.00000  :  +000.00000  % 

     NVC  :  0.01701000  :  0.01750964  :  0.01701000  :  0002.87701  :  +000.00000  :  +000.00000  :  -000.00000  % 

     PPC  :  0.00672111  :  0.00694357  :  0.00672119  :  0007.40972  :  +000.00000  :  +000.00000  :  -000.97552  % 

     QRK  :  0.00011400  :  0.00012109  :  0.00011898  :  0026.21847  :  -000.00000  :  -000.63026  :  -001.20481  % 

     TRC  :  0.00051000  :  0.00052499  :  0.00051000  :  0000.44749  :  +000.00000  :  +000.00000  :  -000.00000  % 

     WDC  :  0.00039301  :  0.00041999  :  0.00042649  :  0033.60477  :  -000.00000  :  -000.00000  :  -000.00000  % 

     XPM  :  0.00384000  :  0.00388991  :  0.00384000  :  0002.67047  :  -000.00000  :  +000.00000  :  -000.22835  % 




Memory Issues
-------------

Lately I recognized that vcx used much more memory than needed. This should be fixed by now.

Normally vcx should stay under 500MB or RAM usage. This amount of memory is needed because vcx stores
the last 500 info-hashes about every currency on vircurex.
