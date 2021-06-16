### ssh into application server using appropriate credentials
$: ssh user@appsvr

### Confirm current timezone setting on server
$: timedatectl

### Check for the correct name for the new timezone
$: timedatectl list-timezones

### Set new timezone on server
$: sudo timedatectl set-timezone <new_timezone_setting>

### Confirm new timezone setting
$: timedatectl
