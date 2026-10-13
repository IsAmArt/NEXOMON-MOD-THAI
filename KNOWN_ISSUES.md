# ข้อจำกัดที่ทราบ / Known Issues

ผู้พัฒนายืนยันว่าเล่น **เนื้อเรื่องหลักและเนื้อหาเสริมช่วงท้ายเกม** ด้วยมอดภาษาไทยจนจบแล้ว ไม่พบปัญหาด้านระบบที่ขัดขวางการดำเนินเนื้อเรื่อง และทดลองติดตั้ง RC บน Notebook อีกเครื่องแล้วสามารถเปิดใช้งานได้

**RC NOTEBOOK INSTALL / LAUNCH = USER-CONFIRMED PASS**

ผลนี้เป็นการยืนยันการติดตั้ง/เปิดใช้งานและเส้นทางการเล่นที่ผู้พัฒนาทดสอบ ไม่ใช่การยืนยันครบทุกภารกิจหรือทุกหน้าจอ ยังจับ Nexomon ในตำนานช่วงท้ายไม่ครบทุกตัว และยังไม่ได้ตรวจทุกกรณีหลังจากนั้น จึงยังไม่ยืนยันว่าจะมีเนื้อเรื่องเพิ่มเติมหรือไม่

## ข้อที่ยังติดตาม

- บางประโยคยังอาจต้องปรับให้เข้ากับบริบท รวมถึงการตัดคำและการขึ้นบรรทัดใหม่ในบางจุด ผู้พัฒนาทำมอดในเวลาว่าง และตั้งใจทยอยตรวจแก้ในเวอร์ชันถัดไปเมื่อสะดวก โดยยังไม่กำหนดวันอัปเดตครับ
- บางหน้าจอหรือกรณีย่อยยังไม่ได้ตรวจ font fallback ครบ หากไม่ได้ขัดขวางการเล่น ไม่จำเป็นต้องเป็น release blocker
- Warden: **TA Font visually confirmed** — ไม่ขยายผลเป็นการตรวจทุกขนาด/ทุกบทพูด
- Volleyball: **manual retest pending**
- Expansion popup: **manual retest pending**
- ชื่อ Nexomon และชื่อทักษะคงภาษาอังกฤษตามต้นฉบับ; คำอธิบายทักษะภาษาไทย 139 ชุด ข้อความอังกฤษบางจุดใช้ fallback โดยตั้งใจ
- เลเวลที่เคยได้จาก QA x8 ในเซฟเดิมไม่ถูกย้อนกลับ; Release DLL ไม่มีตัวคูณ EXP
- มอดภาษา/ฟอนต์อื่นที่แก้ renderer เดียวกันอาจต้องตรวจ compatibility เพิ่ม

## English

The developer has completed the **main story and late-game additional content** using the Thai mod, with no system issue blocking story progression in that playthrough. The RC was also installed and launched successfully on a second notebook.

**RC NOTEBOOK INSTALL / LAUNCH = USER-CONFIRMED PASS**

This confirms installation/launch and the paths played, not exhaustive regression coverage. Not all late-game Legendary Nexomon have been caught, and every subsequent case has not been checked. Any further story content after those activities remains unconfirmed.

Some sentences may still need contextual polishing, and word wrapping or line breaks may be awkward in places. Development is done in spare time; further refinements are intended for a later version when time permits, without an update date being promised.

Warden: TA Font visually confirmed. Volleyball: manual retest pending. Expansion popup: manual retest pending. Some fallback screens and individual cases still need checking; unconfirmed fallback is not automatically a release blocker when it does not impede gameplay. English Nexomon/skill names are intentional. Existing QA-earned levels are retained; the Release DLL has no EXP multiplier. Compatibility with other language/font mods has not been established.
