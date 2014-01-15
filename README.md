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

    15.01.2014 - 20:28:59 - refresh approx. every 5 seconds (+/- some seconds for network latency and server load)
    HB - highest bid / LA - lowest ask / LT - last executed trade / VOL_BTC - Trading Volume in BTC
    TENDENCY is a percentual value and will appear after some time (4.5m), please be patient :)
    Tendency calculates like this: (last_trade / average_of_20_or_50_last_recorded_trades * 100) - 100

    CUR  :          HB  :          LA  :          LT  :     VOL_BTC  :     TEND_20  :     TEND_50
    DGC  :  0.00040500  :  0.00041265  :  0.00040500  :  0001.65512  :    +0.00000  :    +0.00000  % 
   DOGE  :  0.00000048  :  0.00000049  :  0.00000048  :  0081.00274  :    +0.00000  :    +0.33445  % 
    DVC  :  0.00000049  :  0.00000050  :  0.00000050  :  0016.91328  :    -0.00000  :    +0.00000  % 
    FTC  :  0.00040402  :  0.00040996  :  0.00040402  :  0001.87329  :    -0.99500  :    -0.79759  % 
    LTC  :  0.02930002  :  0.02949983  :  0.02930001  :  0018.31709  :    +0.00000  :    -0.00000  %



Have fun!
