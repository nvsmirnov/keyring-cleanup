# GNOME Keyring Cleanup

This script will show gnome keyring entries, or clean keyring out of specified records.
Idea of how to work with keyring is from https://github.com/mnagel/gnome-keyring-dumper

## Prepare

The script uses python 3.

First, install package for python module secretstorage, example is for debian based:
* sudo apt-get install python3-secretstorage

## Usage

keyring-cleanup -h

## Example

To list all saved openconnect passwords:
keyring-cleanup --include-label '(?i)openconnect' --include-attr 'vpn_uuid:.*'
add -c to delete found records, or -v and -s to show full attributes and secrets respectively.