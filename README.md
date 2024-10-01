# UpgradeMediaWikiPlaybook
An Ansible Playbook to update MediaWiki from one version to the next.

* Written for Ubuntu and Apache2
* Assumes the root of the MediaWiki install is in /var/www/virtual/mediawiki-X.XX.X/
* Switch versions by updating /etc/apache2/sites-available/001-wiki.conf to point to the new document root.
* The output of the update command is captured and written to a log on the server in /tmp/

Vars to update depending on old and new version numbers:
* mediawiki_download_file: the filename of the download in the form : "mediawiki-Y.YY.Y"
* mediawiki_download_dir: the directory name in the download URL in the form "Y.YY"
* mediawiki_old_dir: the name of the existing mediawiki directory on disk in the form "mediawiki-X.XX.X"
* update_command: The command to run after the update is complete. This changed between 1.39 & 1.40

Written by Jon Russell September 2024
