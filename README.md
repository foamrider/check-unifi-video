# check-unifi-video
Script for checking Unifi Video last recording and connection state for all cameras, to be used with Nagios

File: check_unifivideo
Parameters:
            https://<unifi-video-address>:<port> -> The URL for Unifi Video UI
            <api-key from Unifi Video> -> API key from Unifi Video (User setting)
            <boolean-status-only> -> false = check both connection status and last recording time, true = check only connection status
            <ignore-camera-name>,<ignore-camera-name2> -> Comma separated list over cameras to ignore
Example:
`./check_unifivideo.php https://192.168.1.20:7443 uyakfgagyeakrsyvcsak false UVC-G3-OUTSIDE,UVC-G3-OUTBACK`

Notes:
* To use ignore parameter, cameras must have unique name (or just change the code to use MAC address instead), separated by comma
* API key can be retrieved from Users in Unifi Video UI

Requirements: php, php-curl, php-json

Tested on PHP 5.3
