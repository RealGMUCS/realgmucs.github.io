

## Network
### VPN (GMU VPN on Linux without Cisco Secure Client)

You can use Linux's built-in NetworkManager VPN support with OpenConnect instead of installing Cisco Secure Client provided by GMU.

#### Install OpenConnect

> You likely already have all these packages installed if you are using KDE or GNOME.

- Debian / Ubuntu

    ```bash
    sudo apt update
    sudo apt install network-manager-openconnect network-manager-openconnect-gnome
    ```

- Fedora

    ```bash
    sudo dnf install NetworkManager-openconnect NetworkManager-openconnect-gnome
    ```

#### Configure the VPN

1. Open **Settings → Network → VPN → +**
2. Choose **Multi-protocol VPN client (OpenConnect)**
3. Set the gateway to:

    ```text
    vpn.gmu.edu
    ```
3. Select *General* (should automatically selected)

4. Connect and authenticate with your *GMU NetID* (e.g., tvn,  no @gmu.edu) and *Duo* (it will send you an authentication on Duo) as usual.

#### Optional: Connect from the terminal

- Debian / Ubuntu

    ```bash
    sudo apt install openconnect
    ```
- Fedora

    ```bash
    sudo dnf install openconnect
    ```
- Then connect with:  

    ```
    sudo openconnect --protocol=anyconnect https://vpn.gmu.edu/general
    ```

This lets you access the GMU VPN on Linux without installing Cisco Secure Client.
