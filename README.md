# Color Roll — Hand Tracking Camera Game

## อัปโหลดเข้า GitHub Pages
1. แตกไฟล์ ZIP นี้ก่อน
2. เปิด repository บน GitHub แล้วเลือก Add file → Upload files
3. อัปโหลด index.html และโฟลเดอร์ vendor พร้อมไฟล์ข้างในทั้งหมดไว้ระดับบนสุดของ repository (ไม่ต้องอัปโหลด ZIP)
4. Commit changes
5. ไป Settings → Pages → Deploy from a branch → main → / (root) → Save
6. เปิดลิงก์ GitHub Pages ที่ได้ กด Enable camera & play แล้วอนุญาตกล้อง

## วิธีเล่น
- ตั้งโทรศัพท์ให้นิ่ง ให้กล้องเห็นมือทั้งมือในที่สว่าง
- รอ HAND TRACKER READY แล้วเปิดกล้อง
- ใช้นิ้วชี้แตะลูกบอลบนภาพกล้อง จากนั้นเลื่อนมือพาลูกบอลลงกล่องสีเดียวกัน
- แดงอยู่ซ้าย น้ำเงินอยู่ขวา
- NO HAND หมายถึงยังไม่พบมือ
- หากโหลดไม่สำเร็จ กด Retry tracker
- Demo mode เล่นด้วยการแตะกล่องหรือปุ่มลูกศร ไม่มีการจับมือ

## Files
- index.html: game and interface
- vendor/vision_bundle.mjs: MediaPipe Tasks Vision 0.10.21
- vendor/wasm/: SIMD and non-SIMD runtime
- vendor/hand_landmarker.task: Google MediaPipe Hand Landmarker model

No build or API key is required. Paths are relative for GitHub Pages project sites.
Camera requires HTTPS (GitHub Pages) or localhost. Opening index.html directly is not supported.
Camera frames are processed locally; no video is recorded or uploaded.
The model was verified to load in Chrome. Live hand tracking needs testing with your own camera.

MediaPipe: https://github.com/google-ai-edge/mediapipe (Apache-2.0).
Hand Landmarker documentation: https://ai.google.dev/edge/mediapipe/solutions/vision/hand_landmarker/web_js
