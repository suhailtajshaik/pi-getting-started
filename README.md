# Raspberry Pi - Get Started without Keyboard, Mouse or Monitor

### Steps: 
1. Download latest Raspberry Pi OS (previously called Raspbian) 
    >Link to download : https://www.raspberrypi.org/downloads/

2. Download Etcher (This software is required to burn Raspberry Pi OS image on to SD Card)
    >Link to download Etcher : https://etcher.io/

3. Format your SD Card and burn Raspberry Pi OS image on to SD Card using Etcher. 

4. Create `ssh` file on root level of SD Card 
    ```bash 
    touch ssh
    ```

5. Create `wpa_supplicant.conf` file on root level of SD Card
    ```bash
    touch wpa_supplicant.conf
    ```
 
6. Edit file `wpa_supplicant.conf` 
   ```bash
    country=US
    update_config=1
    ctrl_interface=/var/run/wpa_supplicant

    network={
        scan_ssid=1
        ssid="ssid"
        psk="password"
    }
   ```
    > List of country codes (Alpha-2 code) : https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2#Officially_assigned_code_elements
