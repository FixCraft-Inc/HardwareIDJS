<pre>
 ALL RIGHTS RESERVED
 _______ _        ______             ___      
(_______|_)      / _____)           / __)_    
 _____   _ _   _| /       ____ ____| |__| |_  
|  ___) | ( \ / ) |      / ___) _  |  __)  _) 
| |     | |) X (| \_____| |  ( ( | | |  | |__ 
|_|     |_(_/ \_)\______)_|   \_||_|_|   \___)
                                              
                                                           
FixCraft® Inc. HardwareIDJS Copyright ©   
Version - v1.0 😎 Jun 19 2024
By F1xGOD 💀
Donate Crypto (Monero)
48BKksKRWEgixzz1Yec3BH54ybDNCkmmWHLGtXRY42NPJqBowaeD5RTELqgABD1GzBT97pqrjW5PJHsNWzVyQ8zuL6tRBcY
</pre>

![GitHub license](https://img.shields.io/github/license/FixCraft-Inc/HardwareIDJS?style=flat)
![GitHub issues](https://img.shields.io/github/issues/FixCraft-Inc/HardwareIDJS?label=Issues)
![GitHub stars](https://img.shields.io/github/stars/FixCraft-Inc/HardwareIDJS)
![GitHub forks](https://img.shields.io/github/forks/FixCraft-Inc/HardwareIDJS)
[![Discord](https://img.shields.io/discord/1130897522051788821?color=7289da&label=Discord&logo=discord&logoColor=ffffff)](https://discord.gg/3eRHYkjgk8)
[![Patreon](https://img.shields.io/endpoint.svg?url=https%3A%2F%2Fshieldsio-patreon.vercel.app%2Fapi%3Fusername%3DF1xGOD%26type%3Dpatrons)](https://patreon.com/F1xGOD)

---

# HardwareIDJS

**⚠️ CLOSED SOURCE**  

`hardwareidjs` is a JavaScript module for generating a **persistent, high-entropy hardware fingerprint** of the client device.  
It combines multiple sources of entropy:  

- **Advanced fingerprinting** using browser APIs (Canvas, WebGL, AudioContext, fonts, screen, timezone, etc.)  
- **Performance & graphics identifiers** (GPU vendor/renderer, WebGL unmasked info)  
- **Platform and UA parsing** (OS, CPU arch, browser details)  
- **Hashing & obfuscation** via SHA-256 (multiple passes, salted with combined info)  

## Usage  

```js
import { getHWID } from './hardwareid.js';

(async () => {
  const hwid = await getHWID();
  console.log('Device HWID:', hwid);
})();
```

`getHWID()` returns a **Promise<string>** containing the hashed hardware ID.  

## Notes  

- The generated ID is **deterministic per device/browser** but resistant to trivial spoofing.  
- No personally identifiable information (PII) is stored directly — only hashed fingerprints.  
- Changing hardware, browser settings, or privacy features may alter the output.  
- The full fingerprinting logic is **proprietary** and **should not be disclosed** publicly.  
