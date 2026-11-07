Naim M3U Playlist & Channel Manager — Android Studio Project

এই ফোল্ডারটি APK তৈরির Android Studio project। এটি নিজে APK ফাইল নয়।

প্রাথমিক সেটিং:
- Minimum Android: 7.0 (API 24)
- Target Android: 15 (API 35)
- App name: Naim M3U Playlist & Channel Manager
- Application ID: com.naim.m3u

APK বানানোর ধাপ:
1. কম্পিউটারে Android Studio ইনস্টল করুন।
2. Android Studio > Open নির্বাচন করে এই project folder খুলুন।
3. Gradle sync শেষ হতে দিন (ইন্টারনেট লাগবে; Android SDK 35 ও Gradle plugin ডাউনলোড হবে)।
4. Build > Build Bundle(s) / APK(s) > Build APK(s) চাপুন।
5. APK তৈরি হলে Android Studio-র notification থেকে Locate চাপুন।

গুরুত্বপূর্ণ:
- এই পরিবেশে Android SDK/Gradle build tool নেই, তাই এখানে APK compile বা ফোনে install-test করা হয়নি।
- ওয়েবসাইটের HTML ফাইল অ্যাপের ভেতরে রাখা হয়েছে।
- ওয়েব ব্রাউজারের localStorage ডেটা Android অ্যাপের আলাদা storage-এ স্বয়ংক্রিয়ভাবে আসবে না। পুরোনো playlist/চ্যানেল দরকার হলে অ্যাপের ভেতরে M3U backup import করতে হবে, অথবা Supabase sync আলাদাভাবে যাচাই/কনফিগার করতে হবে।
- কিছু IPTV stream CORS, provider restriction, expired URL বা codec-এর কারণে নাও চলতে পারে।
- Android 7+ লক্ষ্য করা হয়েছে; সব Android ফোনে শতভাগ সামঞ্জস্যের নিশ্চয়তা নেই।

স্বয়ংক্রিয় APK তৈরি (GitHub Actions):
১) এই ZIP ফাইলটি Extract করুন।
২) GitHub-এ নতুন একটি Repository তৈরি করুন (যেমন: naim-m3u-android)।
৩) ZIP-এর ভেতরের Naim-M3U-Android-Project ফোল্ডারের সব ফাইল/ফোল্ডার Repository-র মূল জায়গায় Upload করুন। .github ফোল্ডারটিও অবশ্যই Upload করবেন।
৪) GitHub Repository-তে Actions ট্যাব খুলুন। “Build Naim M3U APK” workflow নির্বাচন করে “Run workflow” চাপুন।
৫) কাজ সফল হলে workflow run-এর নিচে Artifacts থেকে Naim-M3U-Playlist-Channel-Manager-APK.zip ডাউনলোড করুন। ZIP খুললে app-debug.apk পাবেন।
৬) APK ফোনে ইনস্টল করার আগে Android-এর “Install unknown apps” অনুমতি দিতে হতে পারে।

নোট: এটি Debug APK। Google Play Store-এ প্রকাশের জন্য আলাদা signed release build দরকার। এই workflow APK build করার ব্যবস্থা করে; build সফল হয়েছে—এমন দাবি নয়।
