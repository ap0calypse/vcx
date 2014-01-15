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


