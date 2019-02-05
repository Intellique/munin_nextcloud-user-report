# NAME

nxur - NextCloud user report Munin module
This is a munin plugin used to monitor NextCloud Users storage consumption. 

# CONFIGURATION

This munin plugins requires the NextCloud plugin "User usage report" to be set up first in your NextCloud installation. It's part of the default set of available NextCloud applications or can be downloaded from: https://github.com/nextcloud/user\_usage\_report

This plugin must run as the same user as the webserver.
insert into /etc/munin/plugin-conf.d/munin-node:

        [nxur*]
        user www-data
        group www-data

Default mode displays per user quota usage. To display absolute storage use per
user, name the link nxur\_abs

        ln -s /usr/share/munin/plugins/nxur \
                /etc/munin/plugins/nxur_abs

# AUTHOR

Intellique dev team <dev@intellique.com>

Copyright (c) 2019 Intellique

# LICENSE

GPLv3
