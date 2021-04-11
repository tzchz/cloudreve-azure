Cloudreve for Azure Web Apps

【Step1】
WEBSITES_ENABLE_APP_SERVICE_STORAGE='true'

【Step2】
```YML
version: '3'

services:
  dreve:
    image: jialezi/cloudreve:sp
    restart: always
    volumes:
      - ${WEBAPP_STORAGE_HOME}/cloudreve-data:/root/cloudreve
```

【Step3】
```BASH
wget -P /home/cloudreve-data/ https://cloudreve-bin.tzchz.vercel.app/cloudreve
wget -P /home/cloudreve-data/ https://cloudreve-bin.tzchz.vercel.app/cloudreve.db
wget -P /home/cloudreve-data/ https://cloudreve-bin.tzchz.vercel.app/conf.ini
```

【Step4】
Restart the App.

USERNAME='admin@cloudreve.org'
PASSWORD='7Ep6EfLC'
