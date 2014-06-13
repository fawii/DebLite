### DebLite Readme

DebLite is a free collection of shell scripts for rapid deployment of
LAMP and LNMP stacks (Linux, Apache/Nginx, MySQL and PHP) for Debian. 

DebLite scripts automate configuration of servers for web hosting,
so your websites can be online within minutes! Ideal for those who
prefer hosting sites on their own server without resorting to expensive
and bloated control panels.

The following are installed:-

-   Apache2 with mpm\_event or Nginx
-   MySQL or MariaDB
-   PHP-FPM + commonly used PHP modules
-   Dropbear SSH server
-   Postfix mail server (securely configured to be outgoing only)
-   Varnish cache (optional)

### Quick Install (Git)

    # Install git and clone DebLite
    aptitude install git
    git clone https://github.com/fawii/DebLite.git
    cd DebLite
    
    # Edit options to enter server IP, MySQL password etc.
    vi options.conf
    
    # Make all scripts executable.
    chmod 700 *.sh
    chmod 700 options.conf
    
    # Install LAMP or LNMP stack.
    ./install.sh
    
    # Add a new Linux user and add domains to the user.
    adduser johndoe
    ./domain.sh add johndoe yourdomain.com
    ./domain.sh add johndoe subdomain.yourdomain.com
    
    # Install Adminer or phpMyAdmin
    ./setup.sh dbgui
    
    # Enable/disable public viewing of Adminer/phpMyAdmin
    ./domain.sh dbgui on
    ./domain.sh dbgui off

### Requirements

-   Supports Debian 6 and 7.
-   A server with at least 80MB RAM. 128MB and above recommended.
-   Basic Linux knowledge. You will need know how to connect to your
    server remotely.
-   Basic text editor knowledge. For beginners, learning GNU vi is
    recommended.

