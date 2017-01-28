# PyOpenload

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/42d0f198fcbe43daae71e21b6a3540fe)](https://www.codacy.com/app/mohan3d94/PyOpenload?utm_source=github.com&utm_medium=referral&utm_content=mohan3d/PyOpenload&utm_campaign=badger)

python wrapper for [Openload.co](https://openload.co) [API](https://openload.co/api).

## Install
``` sh
pip install pyopenload
```

## Usage
All methods return python dictionary
``` python
from openload import OpenLoad

openload = OpenLoad('login', 'key')

# User email
account_info = openload.account_info()
print(account_info['email'])

# Download Ticket
download_data = openload.prepare_download('file_id')
print(download_data['ticket'])                          
print(download_data['captcha_url'])                     
                     
# Download Link
download_url_data = openload.get_download_link('file_id', 'ticket', 'captcha_response')
print(download_url_data['name'])                        
print(download_url_data['url'])                         

# Upload file
openload.upload_file('file_path')
    
```

## TODO
- [ ] Tests
