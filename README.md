vcx
===

vcx is a vircurex live ticker that gives you the current statistics of crypto currencies as well 
as your current balances. It needs to be said, that this tool is in a VERY early alpha stage and
should not be trusted to work flawlessly. Although I always try to kill as many bugs as possible,
there is always a slight chance of failure. :)

That said: Use it! Tell me how to make it better! (or do it yourself and send a patch)


Prerequisites:
--------------

In order to run this script your need the following Perl modules installed:

    LWP::UserAgent
    XML::Simple
    LWP::UserAgent::Protocol::https
    Digest::SHA


If you have ArchLinux running, just install everything with this command:


    sudo pacman -S perl-lwp-protocol-https perl-xml-simple perl-libwww


This script is very minimalistic. Please 
edit the script itself and set the @watchlist to whatever you need. For example,
if you want to see only DOGE and LTC stats:

    my @watchlist = qw(DOGE LTC);


Configuration:
--------------

The package includes a sample config file which should be copied to ~/.vcxconf.xml and edited to fit your needs.
For different refresh intervals, you have to start vcx with any decimal value (./vcx 10 for example for 10 secs).


Memory Issues
-------------

Lately I recognized that vcx used much more memory than needed. This should be fixed by now.

Normally vcx should stay under 500MB or RAM usage. This amount of memory is needed because vcx stores
the last 500 info-hashes about every currency on vircurex.
