# linwg
A shell script for quickly and remotely setting up a WireGuard server and generating client configs.

## Installation:

Dependencies:
* `wireguard-tools`
* `ssh`
* `qrencode` (*Optional.* For generating QR code images)

1. Download the `linwg` script: `wget https://raw.githubusercontent.com/iguanajuice/linwg/main/linwg`
2. Make executable: `chmod +x linwg`
3. Move it into your path: `sudo mv linwg /usr/local/bin`

## How-to:

You will need:
* An account with a VPS provider (e.g. Linode)
* An SSH public key

*The following instructions will be for Linode specifically,
but these steps can be adapted for other VPS providers:*

1. Create a new Linode/instance
2. Leave image as Debian
3. Select your desired region
4. Under "Linode Plan" select "Shared CPU" and "Nanode 1 GB"
5. Set a root password (*use your browser's password generator so it'll auto-complete next time*)
6. Under "SSH keys" check your SSH key. If none are listed, add your SSH public key.
7. Scroll to the bottom and click "Create Linode"
8. Wait for your Linode to fully boot
9. Copy it's IPv4 address and run the command `linwg [IP_ADRESS_WITHOUT_BRACKETS]`
10. To connect to the server, run `linwg wg1`
11. To disconnect, repeat the above command (if *not* using NetworkManager)
