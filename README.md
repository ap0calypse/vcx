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

        HB - highest bid / LA - lowest ask / LT - last executed trade / VOL_BTC - Trading Volume in BTC

        CUR  :          HB  :          LA  :          LT  :     VOL_BTC
        DGC  :  0.00039000  :  0.00040700  :  0.00039000  :  0001.28258
        DOGE  :  0.00000047  :  0.00000048  :  0.00000047  :  0050.96187
        DVC  :  0.00000049  :  0.00000050  :  0.00000049  :  0016.61661
        FTC  :  0.00039501  :  0.00040401  :  0.00039500  :  0002.16796
        LTC  :  0.02930004  :  0.02949999  :  0.02950000  :  0016.55296



Have fun!
