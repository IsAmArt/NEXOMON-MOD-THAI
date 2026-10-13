# คู่มือปรับขนาดภาษาไทย — Release Candidate

ปิดเกมก่อนแก้ BepInEx/config/th.modthai.nexomon.phase2.cfg สำรองไฟล์ไว้คนละชื่อก่อน เปิดด้วย Notepad และแก้เฉพาะ Value หลัง = แล้วบันทึก เปิดเกมใหม่เพื่อให้มีผล ค่าเป็นตัวคูณ ไม่ใช่จำนวน pixel; ใช้จุดทศนิยม เช่น 1.10 และเปลี่ยนทีละค่าเล็กน้อย

Release config เก็บ 95 keys เดิมทั้งหมดที่ไม่ใช่ EXP ไม่ยุบ alias เพราะอาจกระทบขนาด ฟอนต์ Regular/Bold และ best-fit ไม่เปลี่ยน ทั้ง [Thai.*] กับ alias เก่าถูก bind แต่เมื่อมี key ใหม่อยู่แล้ว key ใหม่ชนะค่าเก่า ให้แก้ [Thai.*] ไม่แก้ alias เก่าเพื่อหวังให้ key ใหม่เปลี่ยนเอง

## Quick reference — keys ที่ใช้จริง

| กลุ่ม | Section / Key | baseline | ผล |
|---|---|---:|---|
| Global | Thai.Global / Enabled | true | เปิด scaling เฉพาะภาษาไทย |
| Global | Thai.Global / GlobalScale | 1.1 | ทุก mapped role รวม NGUI |
| Unity UI | Thai.Global / UiScale | 1.1 | Unity UI และ Volleyball |
| Bold UI | Thai.Global / BoldScale | 1.2 | Bold UI ยกเว้น inventory item-name ที่ล็อก role |
| Dialogue | Thai.Dialogue / DialogueScale | 1.1 | dialogue body |
| Dialogue/Choice | Thai.Dialogue / ScreenScale | 1.15 | dialogue body/choice group |
| Choice | Thai.Dialogue / ChoiceScale | 1.15 | mapped choices |
| Narration | Thai.Narration / NarrationScale, ScreenScale | 1.2 / 1.2 | narration |
| Notification | Thai.Notification / NotificationScale, ScreenScale | 1 / 1 | notification |
| Inventory | Thai.Inventory / ScreenScale | 1.2 | mapped inventory group |
| Inventory | Thai.Inventory / CategoryScale, ItemNameScale | 1.2 / 1 | heading / item names |
| Buttons | Thai.Role.Bold / ButtonScale | 1 | generic mapped short buttons |
| NexoPad | Thai.NexoPad / TabScale, ScreenScale | 1 / 1 | main tabs / legacy group |
| Team | Thai.Team / ScreenScale, SidebarScale, HeaderScale, StatScale | 1 / 1 / 1 / 1 | mapped team groups |
| Skill | Thai.Skill / DescriptionScale, CostScale | 1.2 / 1 | skill description / cost |
| Database | Thai.Database / ScreenScale, ElementScale, EvolutionScale | 1.2 / 1 / 1.2 | mapped database info |
| Popup | Thai.Popup / BodyScale, ScreenScale | 1 / 1 | popup body/group |
| Save popup | Thai.SaveLoad / PopupScale | 1 | save/load confirmation |
| Battle | Thai.Battle / ScreenScale | 1 | mapped battle UI |

กลุ่มที่มีชื่อเหมือนกันอาจไม่ถูกใช้กับทุกข้อความในหน้าจอ ห้ามคาดว่า scale ทั้งหน้าจะเท่ากัน Inventory names ใช้ Bold แต่ขนาดรักษาสูตรของ role เดิม ScreenScale และ role scale คูณกัน ไม่ใช่ใช้เพียงค่าหนึ่ง [Profile], [Party], [Battle], [Shop] บาง legacy role สงวนไว้จน mapping ยืนยัน ไม่แนะนำให้ใช้เป็นปุ่มปรับทั้งหน้าจอ

คืนค่าก่อนหน้า: ปิดเกม คัดลอก config สำรองทับไฟล์ของมอด แล้วเปิดใหม่ ไม่ลบ config เพื่อคืนค่า เพราะ DLL จะสร้างค่า default ซึ่งอาจไม่เหมือน baseline ที่ต้องการ ค่าตัวคูณถูก clamp 0.50–2.00; ไม่เปลี่ยน font-role เพื่อแก้ clipping ให้ใช้ scale เฉพาะ role และดูภาพจริง

No EXP customization exists in this release. Font size behavior remains conditional on Thai text/language and preserves English restoration. Actual pixel sizes depend on original renderer size, resolution and best-fit; offline checks do not certify visual clipping.
