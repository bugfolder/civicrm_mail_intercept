CiviCRM Mail Intercept
============================

This module allows the interception of CiviCRM-attempted emails in development,
with the option to display the contents in the current page or to dump them to
a file in the `/tmp` directory.

Note, however, that this only applies to emails generated via user interaction with the site, not during CiviCRM cron calls, because CiviCRM's cron processor doesn't do a full bootstrap of Backdrop.

If we're writing to the screen, then the module checks to see if the devel
module is enabled; if it is, we use `dpm()` to format the message on the screen.
Otherwise, it is dumped via `drupal_set_message()`.

This module should be disabled on production and enabled on sandbox or test
sites to prevent sending out real emails.

Installation
------------

- Install this module using [the official Backdrop CMS instructions](https://backdropcms.org/guide/modules).

- Visit the configuration page at Administration > Configuration > Development >
  CiviCRM Mail Intercept (/admin/config/devel/civicrm-mail-intercept) to choose how to handle disabled mail.
  
Documentation
-------------

Additional documentation is located in [the Wiki](https://github.com/backdrop-contrib/civicrm_mail_intercept/wiki/Documentation).

Issues
------

Bugs and feature requests should be reported in [the Issue Queue](https://github.com/backdrop-contrib/civicrm_mail_intercept/issues).

Current Maintainers
-------------------

- [Robert J. Lang](https://github.com/bugfolder)

Credits
-------

- Written for Backdrop CMS by [Robert J. Lang](https://github.com/bugfolder).

License
-------

This project is GPL v2 software.
See the LICENSE.txt file in this directory for complete text.

