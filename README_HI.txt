QuizBattleWar — Yellow Strike (Updated Bundle)

Files:
- index.html : Game app. Admin Panel se Firebase par publish ki gayi music URL ko read karke play karne ke liye update kiya gaya hai.
- admin.html : Separate admin page; Gemini question generation feedback aur music upload UI included.
- storage.rules : Firebase Storage rules for admin music uploads.

Important setup:
1. GitHub repo mein game wali site ke root par index.html replace karein.
2. Adminf repo/site ke root mein admin.html ko index.html naam se upload karein, agar aapka GitHub Pages URL /Adminf/ root page kholta hai. Purani file ka backup rakhna.
3. Firebase Console > Storage mein Storage enable karein (agar pehle se enabled nahi hai). Storage Rules mein storage.rules ka content paste/publish karein.
4. Firebase Console > Authentication > Settings > Authorized domains mein apne GitHub Pages hostname ko add karein.
5. Realtime Database rules mein appSettings ka read public aur write sirf Admin UID ke liye hona chahiye. Existing online match rules ko bina check kiye overwrite na karein.
6. Admin login karein. Gemini key enter karke Generate & Publish dabayein. Agar error aaye to admin page ke status area mein exact error dekhein. API key kisi ko share na karein; public frontend mein key rakhna production ke liye secure nahi hai.
7. Music upload ke liye audio file choose karein, mood set karein, Upload & Save to Game dabayein. Game mein wahi mood select karke Music button dabayein. Browser autoplay policy ke karan pehla play user ke tap se hi hona chahiye.

Testing note:
- HTML inline JavaScript syntax-check ki gayi hai.
- Firebase credentials, Gemini API key, Storage enablement/rules, Google OAuth domain, network access aur live audio playback ko is environment se end-to-end test nahi kiya ja sakta.
- Is bundle ko upload karne ke baad pehle Admin ke Generate & Publish aur Music Upload dono ko test karein. Agar status mein error aaye, exact error text bhejein (API key ko hide karke).
