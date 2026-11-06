# Radhika Cab GPS Fare Meter

## प्रोजेक्टमध्ये काय आहे
- Android Kotlin app source (`app/`)
- GPS foreground location service (START नंतर स्क्रीन बंद/दुसरे अॅप असताना tracking)
- ₹25 प्रति km fare calculation
- END नंतर PAY IN CASH / CASH COLLECTED स्क्रीन
- PDF बिल export
- Codemagic cloud build config (`codemagic.yaml`)

## GitHub वर upload
1. ZIP extract करा.
2. `RadhikaCabGPS` फोल्डरच्या आतली सर्व सामग्री GitHub repository च्या root मध्ये upload करा.
3. `codemagic.yaml` repository root मध्ये असणे आवश्यक आहे.
4. Codemagic मध्ये repository refresh करून `radhika-cab-android` workflow निवडा.
5. Build सुरू करा. APK artifact `app/build/outputs/apk/debug/` मधून मिळेल.

## महत्त्वाच्या सूचना
- Codemagic workflow मध्ये उपलब्ध `gradle` command वापरले आहे; `gradlew`/`gradle-wrapper.jar` आवश्यक नाहीत.
- हा source project आहे, तयार APK नाही. Build आणि फोनवरील GPS/background चाचणी करणे आवश्यक आहे.
- Background GPS साठी Android Location आणि Notifications permissions द्या. फोनच्या Battery settings मध्ये app ला Unrestricted/Don't optimize द्या. Android च्या आवृत्ती व निर्मात्यानुसार background restrictions बदलू शकतात.
- GPS अंतराची अचूकता सिग्नल, इमारती आणि फोनवर अवलंबून असते.
