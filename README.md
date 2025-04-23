
---

**README.txt**  
**Title: Flashing Unlocked Patched System Image to JioFi JMR541**

---

### ⚠️ Disclaimer:
Proceed at your own risk. Flashing firmware can permanently damage your device if not done correctly. Ensure your device is fully charged and you're familiar with Fastboot operations.

---

### 📋 Requirements:
- JioFi JMR541 device with unlocked bootloader  
- ADB & Fastboot drivers installed on your PC  
- Patched `system.img` file located at:  
-  http://xdaforums.com/t/guide-updated-unlocking-jiofi-3-jmr540-jmr541-for-all-networks.4285551/
- USB cable and Windows PC  

---

### 🛠️ Flashing Steps:

1. **Connect Device in Fastboot Mode**  
   - Power off the device  
   - Boot into Fastboot mode (usually by holding reset key which is back side in jiofi and battery should be removed and if three all light will blink then you are good to go...)

2. **Open Command Prompt**  
   - Press `Win + R`, type `cmd`, and hit Enter

3. **Verify Fastboot Connection**  
   ```
   fastboot devices
   ```
   - Your device ID should appear. If not, check drivers and cable.

4. **Erase the Existing System Partition**  
   ```
   fastboot erase system
   ```

5. **Flash the Patched System Image**  
   ```
   fastboot flash system "C:\Users\omkar\Desktop\jiofi\JMR541_unlocked_patched_system\system.img"
   ```

6. **(Skip) Flashing recoveryfs**  
   - This step is intentionally skipped as `system.img` is already flashed.

7. **Reboot the Device**  
   ```
   fastboot reboot
   ```

---

### ✅ Done!
Your JioFi JMR541 should now boot with the unlocked and patched system image.

---
