# ქართული ტექსტის სიტყვის სინთეზი / Georgian-TTS 
ქართული ტექსტის სიტყვის სინთეზი /
Georgian text to speech synthesis
## ეს ნიმუშები გამოიყენება მხოლოდ კვლევისთვის ყოველგვარი კომერციული გამოყენების გარეშე / This samples are used only for research without any commercial usage
# ყველა ნიმუში არის 22050 Hz / All samples are in 22050 Hz

# ხარისხის ანალიზი MOS-ის გამოყენებით / Quality analysis using Mean Opinion Score (MOS)
MOS - მეტრიკა აუდიოს ხარისხის შესაფასებლად, დიაპაზონი არის [0-5] 0 შორის - ცუდი ხარისხი, 5 - იდეალური ხარისხი. \
სინამდვილეში ის ინგლისურ ენაზე იყო მომზადებული, მაგრამ აღმოვაჩინე, რომ სხვა ენებისთვის ის ასევე შეესაბამება ხარისხს. <br /> 
დიაგრამა MOS ქულებით, რომელიც შეფასებულია გენერირებული აუდიოდან test_text.txt ფაილიდან 1000 ფრაზის გამოყენებით, მოცემულია ქვემოთ.\
<br />
MOS - metric for audio quality estimation, range is between [0-5] 0 - Bad quality, 5 - Perfect quality. \
Actually it was trained on English language, but i've found that for other languages it also correlates with quality. <br />
Chart with MOS scores that was estimated from generated audio using 1000 phrases from test_text.txt file is given below.

# შესრულების ანალიზი / Performance analysis
შესრულების შედეგები გამოცდილი იყო GPU RTX 4090 (24 GB) და CPU 13th Gen Intel(R) Core(TM) i9-13900K. \
Ubuntu 22.04.4 LTS \
Box-ის ნახაზები სხვადასხვა რაოდენობის სიმბოლოებით, აუდიო ხანგრძლივობით და მათი დარღვევის დრო Cpu-სა და gpu-ზე მოცემულია ქვემოთ. ქვემოთ მოცემული სქემებიდან და ცხრილიდან ხედავთ, რომ ადვილია მისი რეალურ დროში გამოყენება gpu-ს გამოყენებით.\
<br />
Performance results was tested on GPU RTX 4090 (24GB) and CPU 13th Gen Intel(R) Core(TM) i9-13900K. \
Ubuntu 22.04.4 LTS \
Box plots with different number of characters, audio durations and their infrence time on cpu and gpu is given below. You can see from charts and table below, that it easy to use it in real time using gpu.

# კონტაქტები / Contacts
თუ გაინტერესებთ ქართული TTS მოდელის ტესტირება, გთხოვთ, ნუ მოგერიდებათ მომწეროთ ელექტრონული ფოსტით: icegas555@gmail.com <br /> 
ჩვენ ასევე შეგვიძლია დავლიოთ ფინჯანი ყავა და ვიმსჯელოთ პოტენციურ თანამშრომლობაზე, თუ დაინტერესდებით\
<br />
If you're intersted in testing Georgian TTS model, please don't hesistate to write me by email: icegas555@gmail.com <br /> 
We can also drink a cup of coffe and discuss potential collaboration if you're intersted. 
# Other languages
If you need to create TTS system on another language, i'd like to help, please contact me directly by email.