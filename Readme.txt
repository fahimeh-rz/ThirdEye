flame:/ # mkdir /data/crontab
flame:/ # echo '* * * * * svc wifi enable' >> /data/crontab/root
flame:/ # echo '* * * * * settings put global airplane_mode_on 0' >> /data/crontab/root
flame:/ # echo 'crond -b -c /data/crontab' > /data/adb/service.d/crond.sh
flame:/ # chmod +x /data/adb/service.d/crond.sh
settings put global captive_portal_mode 0 

adb shell content insert --uri content://settings/system --bind name:s:accelerometer_rotation --bind value:i:0
