# टेलीग्राम क्लाइंट

**टेलीग्राम क्लाइंट** एक लाइब्रेरी है जिससे आप वास्तविक समय में टेलीग्राम क्लाइंट के साथ बातचीत कर सकते हैं, जिससे आप अनौपचारिक टेलीग्राम एप्लिकेशन / बॉट / यूजरबॉट बना सकते हैं

- 🇮🇩 [Indonesia](https://github.com/azkadev/telegram_client/blob/main/README.md)
- 🇨🇿 [Afrika](https://github.com/azkadev/telegram_client/blob/main/README_AFRIKA.md)
- 🇨🇳 [China](https://github.com/azkadev/telegram_client/blob/main/README_CHINA.md)
- 🏴󠁧󠁢󠁥󠁮󠁧󠁿 [English](https://github.com/azkadev/telegram_client/blob/main/README_ENGLISH.md)
- 🇮🇳 [India](https://github.com/azkadev/telegram_client/blob/main/README_INDIA.md)
- 🇮🇩 [Jawa](https://github.com/azkadev/telegram_client/blob/main/README_JAWA.md)
- 🇯🇵 [Jepang](https://github.com/azkadev/telegram_client/blob/main/README_JEPANG.md)
- 🇰🇷 [Korea](https://github.com/azkadev/telegram_client/blob/main/README_KOREA.md)
- 🇷🇺 [Russia](https://github.com/azkadev/telegram_client/blob/main/README_RUSSIA.md)
- 🇮🇩 [Sunda](https://github.com/azkadev/telegram_client/blob/main/README_SUNDA.md)
- 🇹🇭 [Thailand](https://github.com/azkadev/telegram_client/blob/main/README_THAILAND.md)

## टेलीग्राम फ़ायर बनाना

इस लाइब्रेरी का उपयोग करने के लिए आपको **api_id** और **api_hash** की आवश्यकता होगी

कृपया अपना स्वयं का https://my.telegram.org/auth बनाएं

## तथ्य

- इस लाइब्रेरी का पुनर्निर्माण किया गया था, क्योंकि शायद अधिकांश अन्य लोग पिछली लाइब्रेरी से भ्रमित थे जो मेरी अपनी निर्भरताओं से बंधी थी, कोई दस्तावेजीकरण नहीं था।

- हमेशा नवीनतम tdlib के साथ अद्यतन ताकि आपको मेरे अद्यतन करने के लिए इंतजार नहीं करना पड़े।

## विशेषता

- [x] **बहुत तेज़** एसिंक्रोनस लाइब्रेरी (**नॉन-ब्लॉकिंग थ्रेड्स**)
- [x] **उपयोग में आसान**

## उदाहरण

- [टीडीलिब ग्राम](https://github.com/azkadev/tdlib_gram)
- [सरल उदाहरण](https://github.com/azkadev/telegram_client/tree/main/quickstart)

## स्थापित करना

इंस्टॉल करने से पहले, सुनिश्चित करें कि आप डार्ट / फ़्लटर की मूल बातें जानते हैं, कम से कम आपने अपने कंप्यूटर / डिवाइस पर फ़्लटर / डार्ट इंस्टॉल किया है। [फ़्लटर वेबसाइट](https://flutter.dev)


- **डार्ट / क्ली केवल, कोई गुई नहीं**
यदि आप इसे GUI के बिना उपयोग करना चाहते हैं तो आपको [Tdlib](https://github.com/tdlib/td) संकलित और स्थापित करने की आवश्यकता है यदि आप संकलित नहीं कर सकते हैं तो आप संकलित लाइब्रेरी को यहां से डाउनलोड कर सकते हैं [Tdlib](https://github.com/azkadev/telegram_client/releases/tag/tdlib) अपने OS के अनुसार खोजें और इसे मैन्युअल रूप से स्थापित करें / इसे अपने प्रोजेक्ट में डालें

```बैश
डार्ट पब ऐड telegram_universe
```

- **स्पंदन गुई**
मूलतः डार्ट के समान ही, अंतर यह है कि आपको tdlib को मैन्युअल रूप से स्थापित करने की आवश्यकता नहीं है
बस कमांड जोड़ें

```बैश
स्पंदन पब tdlib_library जोड़ें
```



## दस्तावेज़ीकरण

### सुनिश्चित करें कि आरंभ किया गया

अनिवार्य विधि को **on** के बाद / **on** विधि से पहले स्वतंत्र रूप से बुलाया जा सकता है, लेकिन मैं **on** से पहले की अनुशंसा करता हूं

**उदाहरण:**

```डार्ट
टेलीग्रामक्लाइंट.ensureInitialized();
```


### आरंभ किया गया

इस विधि को **on** विधि के बाद बुलाया जाना चाहिए क्योंकि इसका उपयोग अद्यतनों को संसाधित करने के लिए किया जाता है।

**उदाहरण:**

```डार्ट
telegramClient.initialized() का इंतजार करें;
```

### पर

यह ऑन विधि invoke / update tdlib से डेटा अपडेट प्राप्त करने के लिए उपयोगी है

**उदाहरण:**

```डार्ट
telegramClient.on("अपडेट", (मैप अपडेट) async {
प्रिंट(अद्यतन);
});
```


### क्लाइंट बनाएं

नया क्लाइंट बनाने के लिए सुनिश्चित करें कि आप विधि को कॉल करें।

**उदाहरण:**

```डार्ट
अंतिम new_tdlib_client_id = telegramClient.createClient();
प्रिंट("नया टीडीलिब क्लाइंट आईडी: ${new_tdlib_client_id}");
```


### आह्वान करें

टेलीग्राम tdlib एपीआई को कॉल करने के लिए आपको सीधे दस्तावेज़ पढ़ने की आवश्यकता है

- [Tdlib दस्तावेज़](https://core.telegram.org/tdlib/docs/classtd_1_1td__api_1_1_function.html) आम जनता के लिए पढ़ने में आसान है
- [Tdlib Tl](https://github.com/tdlib/td/blob/master/td/generate/scheme/td_api.tl) सबसे नया और सबसे उपयोगी है यदि आप नवीनतम tdlib का उपयोग करते हैं जो स्वयं को सीधे संकलित करता है

यहाँ मैं केवल डेटा मैप पैरामीटर प्रदान करता हूँ, इस मैप / json में कई महत्वपूर्ण कुंजियाँ हैं


| कुंजी | विवरण | मूल्य | आवश्यक |
|----------------|------------------------------------------------------------------------------------------------------------------|------|----------------------------------------------------------------------|
| **@प्रकार** | यह tdlib से विधियों से भरा है | **स्ट्रिंग** | **हाँ** |
| **@client_id** | इसमें **createClient** विधि से क्लाइंट आईडी शामिल है | **इंट** | **यदि सिंक विधि के लिएलेग्राम

- **सेटलॉगवर्बोसिटीलेवल**
क्योंकि यह एक लॉग विधि है, आप सिंक विधि का उपयोग करते हैं
और कुंजी **@client_id** भरना अनिवार्य नहीं है

उदाहरण:


```डार्ट
telegramClient.invokeSync(
tdlib_scheme.SetLogVerbosityLevel.create(
new_verbosity_level: 0,
).toJson(),
);
```

- **मेसेज भेजें**
इस लाइब्रेरी का उपयोग करके संदेश भेजने के लिए, सुनिश्चित करें कि क्लाइंट लॉग इन है।
[SendMessage दस्तावेज़ीकरण संदर्भ](https://core.telegram.org/tdlib/docs/classtd_1_1td__api_1_1send_message.html)

```डार्ट

/// createClient या update से प्राप्त करें
int client_id = 1; 
अंतिम getMe = await telegramClient.invoke({
"@type": "getMe",
"@client_id": क्लाइंट_आईडी,
}); 
प्रिंट(getMe); 
telegramClient.invoke({ का इंतजार करें
"@type": "संदेश भेजें",
"@client_id": क्लाइंट_आईडी,
"chat_id": getMe["id"],
"विकल्प": {
"@type": "संदेशभेजेंविकल्प",
"disable_notification": सत्य,
},
"इनपुट_संदेश_सामग्री": {
"@type": "इनपुटमैसेजटेक्स्ट",
"मूलपाठ": {
"@type": "स्वरूपित पाठ",
"text": "नमस्ते दुनिया",
}
}
});
```

उपरोक्त केवल एक उदाहरण है, किसी अन्य विधि का उपयोग करने के लिए, बस पैरामीटर डेटा भरें, सुनिश्चित करें कि पैरामीटर कुंजी को तालिका के अनुसार भरना आवश्यक है, मेरा मतलब है कि कई कुंजियाँ हैं जिन्हें भरना आवश्यक है, यदि नहीं, तो यह त्रुटि डेटा भेजेगा।

## मदद

**कठिन**? मैंने इस लाइब्रेरी को यथासंभव सर्वोत्तम तरीके से बनाया है और इसे पढ़ने और उपयोग करने में यथासंभव आसान बनाने का प्रयास किया है।

यदि **आपको** अभी भी **कठिनाई** और **भ्रम** महसूस हो रहा है तो **बिना किसी शुल्क के** हमारे **समूह** में निःशुल्क शामिल होने का प्रयास करें**

- [टेलीग्राम](https://t.me/DEVELOPER_GLOBAL_PUBLIC)
- [डिस्कॉर्ड](https://discord.gg/h4qanyN7)

**जुड़ने से पहले** सुनिश्चित करें कि आप एक स्पष्ट प्रोफ़ाइल का उपयोग करते हैं**, हमें इससे कोई फर्क नहीं पड़ता कि आप कौन हैं, और आपकी रैंक क्या है, लेकिन **सुनिश्चित करें** कि आपके पास एक उपयोगकर्ता नाम और प्रोफ़ाइल फ़ोटो है**, और समूह में चैट करने का प्रयास करें**, निजी चैट नहीं** क्योंकि यह एक सार्वजनिक समूह है और अन्य लोग भ्रमित हो सकते हैं**। यदि आप इसका पालन नहीं करते हैं, तो संभव है कि आप समूह में चैट तक नहीं पहुंच पाएंगे और आपको प्रतिबंधित कर दिया जाएगा। इसका समाधान दूसरे खाते का उपयोग करना है, क्योंकि प्रतिबंधित होने के बाद हम त्वरित प्रतिक्रिया नहीं दे पाएंगे।


## कोई अन्य समस्या?

क्या आपको नीचे कोई समस्या है?

- **भ्रमित / उपयोग में आसान नहीं**
क्या आप इस प्रोग्राम का उपयोग करने में उलझन में हैं, चक्कर आ रहा है या मतली आ रही है? जटिल tdlib डेटा के कारण?

- **विलंब / व्यवसाय का विस्तार नहीं किया जा सकता**
क्या आपको लगता है कि यह पिछड़ रहा है और इसे व्यवसाय के स्तर तक नहीं बढ़ाया जा सकता?

हां, हमने अपनी तरफ से पूरी कोशिश की है, हम केवल डिफ़ॉल्ट मानकों का पालन करते हैं, यह धीमा नहीं पड़ता है और वास्तव में इसे व्यावसायिक पैमाने के लिए बनाया जा सकता है, लेकिन **tdlib** बहुत भारी है और **I/O** / **मेमोरी** बर्बाद करता है

हां, मैंने इसे अपने निजी व्यवसाय के लिए इस्तेमाल किया है। हां, यह सच है कि इससे संसाधनों की बर्बादी होती है, भले ही मेरा कोड कुशल है और थ्रेड्स को ब्लॉक नहीं करता है। ऐसा कई कारकों के कारण भी होता है, जैसे आपकी कोड शैली और कोड भाषा।

यदि आप अधिक सुविधाएं चाहते हैं और इसे आसानी से व्यावसायिक स्तर पर बनाया जा सकता है, तो आप मेरी इस परियोजना में रुचि ले सकते हैं।

[सामान्य सार्वजनिक भाषा](https://github.com/generalpubliclanguage)

**भाषा** कोड क्या है? यह एक कोड भाषा है जिसे विशेष रूप से आपके लिए किसी भी प्रोजेक्ट को आसानी से बनाने के लिए डिज़ाइन किया गया है और इसमें समझने में आसान कोड शैली और डेटा संरचनाएं हैं जो tdlib से अधिक आसान हैं

कोड भाषा में अंतर्निहित विशेषताएं हैं, इसलिए आपको अपने प्रोजेक्ट में कुछ जोड़ने की आवश्यकता नहीं है।

हम काफी समय से इसकी जांच कर रहे हैं, दरअसल यह समस्या **tdlib** और **dart** दोनों परियोजनाओं में है

टीडीलिब संसाधन-गहन है, डार्ट अनंत लूप थ्रेड्स को अलग करने के लिए भारी है, और मेमोरी को रिलीज करने में भी कई मिनट लगते हैं, इसलिए यदि कई अपडेट हैं तो यह बहुत बेकार है, खासकर यदि व्यवसाय के पैमाने पर कई ग्राहकों की आवश्यकता होती है।

ताकि **सामान्य सार्वजनिक भाषा** कोड भाषा बनाई जा सके और वह आपकी आवश्यकताओं का समाधान हो सके।

यदि आपको लगता है कि मुझे तुरंत अपडेट करने की आवश्यकता है, तो कृपया नीचे दिए गए चरणों का पालन करके मेरी सहायता करें।

## मुझे समर्थन करो

यदि आपको यह कार्यक्रम उपयोगी लगता है, तो आप मुझे [GITHUB AZKADEV](https://github.com/azkadev) उस लिंक में समर्थन कर सकते हैं, मेरे सोशल मीडिया और प्रायोजक उपलब्ध हैं। मुझे कोई आपत्ति नहीं अगर आप बस फॉलो करें / थोड़ा पैसा दान करें

- https://www.patreon.com/c/azkadev
- https://opencollective.com/azkadev
- https://paypal.me/azkaaxeliongibran
- https://paypal.me/azkadev

धन्यवाद


अज़्कादेव - 07-18-2025


## टैग

- tdlib डार्ट
- tdlib स्पंदन
- टेलीग्राम डार्ट
- टेलीग्राम फ़्लटर
- टेलीग्राम क्लाइंट डार्ट
- टेलीग्राम क्लाइंट स्पंदन