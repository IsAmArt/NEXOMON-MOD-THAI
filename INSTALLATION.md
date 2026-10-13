# ติดตั้ง / Installation

1. ใช้ Nexomon PC/Steam ของตนเองบน Windows x64 เวอร์ชันที่ตรวจในเครื่องพัฒนา: Steam App 1191580, build ID 5270054, Unity player 2019.2.8f1 (file version 2019.2.8.16735046) ไม่ต้องติดตั้ง Unity Editor เพื่อเล่นมอด
2. ปิดเกม สำรองโฟลเดอร์ BepInEx/plugins/NexomonThai และ BepInEx/config/th.modthai.nexomon.phase2.cfg เดิม เซฟแยกเก็บไว้นอกโฟลเดอร์เกมได้ แต่แพ็กเกจนี้ไม่มีเครื่องมือจัดการเซฟและจะไม่แตะเซฟ
3. ติดตั้ง BepInEx 5.4.23.5 x64 แยกต่างหากตามคู่มือของโครงการ BepInEx จาก https://github.com/BepInEx/BepInEx/releases เลือกสาย 5 และ x64 ไม่ใช่ BepInEx 6/IL2CPP แพ็กเกจมอดไม่รวม BepInEx/Harmony binaries
4. แตก ZIP เปิดโฟลเดอร์ NexomonThai แล้วคัดลอกโฟลเดอร์ BepInEx ภายในไปที่โฟลเดอร์เกมซึ่งมี Nexomon.exe ไม่ใช่ Nexomon_Data อย่าให้ซ้อนเป็น plugins/NexomonThai/NexomonThai
5. DLL ต้องอยู่ BepInEx/plugins/NexomonThai/NexomonThaiPhase2.dll และมี bundles Regular/Bold, thai_flag_158x101.png, Translations อยู่ข้างกัน
6. สำหรับเครื่องใหม่ ใช้ config ที่ให้มาเพื่อคง typography baseline สำหรับอัปเดต QA เดิม ให้สำรอง config ก่อน ตัดสินใจว่าจะใช้ release config หรือเก็บค่าที่ปรับเอง อย่า reset ทุก scale เป็น 1; old EXP keys ไม่ถูกอ่านโดย Release DLL แล้ว
7. ผู้ใช้เปิดเกมเอง แล้วเลือก THAI จากหน้าต้นเกม ตัวเลือกภาษาไม่มีในเมนูระหว่างเล่น ต้องปิด/เปิดเกมเพื่อสลับ
8. ทดสอบบทพูดที่มี ย้ำ/น้ำ/ซ้ำ, narration/notification, Inventory, NexoPad, choices และ battle UI ตรวจว่า English skill names/Thai descriptions ถูกต้อง
9. ปิดแล้วเปิดใหม่เลือก ENGLISH ตรวจฟอนต์เดิมกลับและไม่มี Thai/PUA ค้าง จด screenshot และ BepInEx/LogOutput.log หากพบปัญหา ตรวจ EXP หลังชนะการต่อสู้ว่าไม่มีตัวคูณจากมอด
10. หากมี regression ให้ปิดเกมและคืน DLL/Translations/config จาก backup เป็นชุดเดียวกัน ไม่แก้ Nexomon_Data หรือเซฟ

Uninstall: close game, remove only BepInEx/plugins/NexomonThai. Back up before optionally removing this mod's config. Keep shared BepInEx used by other mods. No save deletion/reset is required. On update remove stale older copies of this plugin from other plugin folders only after identifying and backing them up; never run two DLL copies with the same GUID.

RC NOTEBOOK INSTALL / LAUNCH = USER-CONFIRMED PASS. ผู้ใช้ยืนยันติดตั้งและเปิดใช้งานบน Notebook อีกเครื่องได้แล้ว ขั้นตอนตรวจหน้าจอ/กรณีย่อยด้านบนยังเป็น checklist ไม่ถือว่าทุกข้อผ่านแล้ว การเผยแพร่เอกสารและแพ็กเกจไม่ใช่การทดสอบเล่นเกมใหม่

## English quick installation

Close Nexomon and back up the old plugin/config. Install BepInEx 5.4.23.5 x64 separately. Extract this ZIP and copy its inner BepInEx folder beside Nexomon.exe. Include the supplied release config on a clean install; back up and deliberately migrate existing customized configs. Select THAI at startup. To switch to ENGLISH, close/reopen the game. Smoke-test dialogue, notifications, Inventory/NexoPad, battle EXP and English font restoration. To uninstall, remove only plugins/NexomonThai; do not remove saves or shared BepInEx used by other mods.
