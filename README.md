# ZKTeco BioTime 8.x - 9.x | Security Analysis & Vulnerabilities

[![Research](https://img.shields.io/badge/Purpose-Security%20Research-red)](https://github.com)
[![Version](https://img.shields.io/badge/Version-8.0--9.x-blue)](https://github.com)
[![License](https://img.shields.io/badge/License-Educational%20Only-yellow)](https://github.com)

> **⚠️ DISCLAIMER:** This repository is for **educational and security research purposes ONLY**.  
> Do not use these techniques on systems you do not own or have explicit permission to test.  
> The author is not responsible for any misuse of this information.
  
## 🔥 Critical Findings (The "Golden Keys")

### Hardcoded AES Keys (V-01)

```python
KEY1 = b'china@2018encryption#aes'
IV1  = b'zkteco@china2019'

KEY2 = b'mMH7L4DFHzo2y8YSgntzfm1x0Z_hFvMA'
IV2  = b'hQHu9xoUeXc=8YSg'

BASE_SECRETE = '=Q6(Zc:7ad>}s6ZF?B7;dTCgHf\\#^G*}(ey:Wc7J6fG@:9YU&D'
SECRET_KEY = BASE_SECRETE[:35] + str(uuid.getnode())[:15]  # MAC address!

(All Versions Affected)
