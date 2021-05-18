# Custom Template for Grandstream HT-81x ATAs

The following is a custom template for the Grandstream HT-81x series of ATAs. This has been tested with the HT-812 and HT-814 on firmware 10.0.25.5. Line configurations have been configured for up to 4 independent lines. You can add Hunt Groups via additional overrides.


# Instructions
## Create Custom Format

 1. In your NDP, navigate to System, then Files and Firmware
 2. Upload [grandstreamHT81x.xml](https://github.com/OITApps/HT81xConfig/blob/main/grandstreamHT81x.xml)
 3. Click on System, then Custom Definitions
 4. Click Add
 5. Format Name: Grandstream HT-81x
 6. Template: grandstreamHT81x.xml
 7. Click Create

## Note Overrides
You will need to modify and add these overrides per device definition. Replace the values within the quotation marks for use in the next section

P2="secure web password"
P133="0 fixed buffer, 1 adaptive" 
P231="Device Mode. 0 -NAT Router, 1 - Bridge"
P824="disable LEC"
P192="firmware path without protocol"
P237="provisioning url without protocol"
P1650="web access mode  0 - HTTPS, 1 - HTTP, 2 - Disabled"

## Create Grandstream HT-812
1. Click on System, then Device Definitions
2. Click Add
3. Brand: Grandstream
4. Model: HT-812
5. Type: Device
6. NDP Code Structure:  Grandstream HT-81x
7. Number of Phone Lines: 2
8. Resync Enabled: yes
9. Show in portal: yes
10. Overrides:  Add overrides from previous section
11. Click Create

## Create Grandstream HT-814
1. Click on System, then Device Definitions
2. Click Add
3. Brand: Grandstream
4. Model: HT-814
5. Type: Device
6. NDP Code Structure:  Grandstream HT-81x
7. Number of Phone Lines: 4
8. Resync Enabled: yes
9. Show in portal: yes
10. Overrides:  Add overrides from previous section
11. Click Create

## Summary
The models will now be available for provisioning from the Manager Portal as a device.
