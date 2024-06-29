# ქართული ტექსტის სიტყვის სინთეზი / Georgian-TTS (Georgian text to speech synthesis)
ქართული ტექსტის სიტყვის სინთეზი /
Georgian text to speech synthesis
## ეს ნიმუშები გამოიყენება მხოლოდ კვლევისთვის ყოველგვარი კომერციული გამოყენების გარეშე / This samples are used only for research without any commercial usage
# ყველა ნიმუში არის 22050 Hz / All samples are in 22050 Hz


https://github.com/icegas/Georgian-TTS/assets/32134483/e387fb0a-5b6b-4d40-8892-1948ff13e4d9 

https://github.com/icegas/Georgian-TTS/assets/32134483/426f9fc8-2d26-44ec-84e3-8b511c9cb51e

https://github.com/icegas/Georgian-TTS/assets/32134483/a40020d5-dfe4-4da7-8fc4-9849a40cb8b5



https://github.com/icegas/Georgian-TTS/assets/32134483/b0c1d7e3-61e5-457e-ba4a-c6d8fa467aa2



https://github.com/icegas/Georgian-TTS/assets/32134483/589fc31e-c648-4128-bd52-4eca140ed05b







https://github.com/icegas/Georgian-TTS/assets/32134483/e7bb0b26-2a78-4e4b-a7ad-441b0c7a0fe2




https://github.com/icegas/Georgian-TTS/assets/32134483/d362e3ca-b309-473b-8c3d-22770400e5e2

# 3 ნიმუში სხვადასხვა სიჩქარით / 3 samples with different speed

https://github.com/icegas/Georgian-TTS/assets/32134483/ac184fc1-94ea-4c5d-9a04-1293ec562e07


https://github.com/icegas/Georgian-TTS/assets/32134483/f55e534a-b4ee-401f-a9bf-f03ebec206be



https://github.com/icegas/Georgian-TTS/assets/32134483/e19d84ee-038e-4da9-ad41-b2c3c510e3cb



# ხარისხის ანალიზი MOS-ის გამოყენებით / Quality analysis using Mean Opinion Score (MOS)
MOS - მეტრიკა აუდიოს ხარისხის შესაფასებლად, დიაპაზონი არის [0-5] 0 შორის - ცუდი ხარისხი, 5 - იდეალური ხარისხი. \
სინამდვილეში ის ინგლისურ ენაზე იყო მომზადებული, მაგრამ აღმოვაჩინე, რომ სხვა ენებისთვის ის ასევე შეესაბამება ხარისხს. <br /> 
დიაგრამა MOS ქულებით, რომელიც შეფასებულია გენერირებული აუდიოდან test_text.txt ფაილიდან 1000 ფრაზის გამოყენებით, მოცემულია ქვემოთ.\
<br />
MOS - metric for audio quality estimation, range is between [0-5] 0 - Bad quality, 5 - Perfect quality. \
Actually it was trained on English language, but i've found that for other languages it also correlates with quality. <br />
Chart with MOS scores that was estimated from generated audio using 1000 phrases from test_text.txt file is given below.

![mos_hist](https://github.com/icegas/Georgian-TTS/assets/32134483/97f4a4cd-29c4-4f5d-9675-def6412a6f4c)


# შესრულების ანალიზი / Performance analysis
შესრულების შედეგები გამოცდილი იყო GPU RTX 4090 (24 GB) და CPU 13th Gen Intel(R) Core(TM) i9-13900K. \
Ubuntu 22.04.4 LTS \
ექსპერიმენტები ჩატარდა სხვადასხვა რაოდენობის სიმბოლოებით, აუდიო ხანგრძლივობით და მათი დასკვნის დრო Cpu-ზე და gpu-ზე და მოცემულია ქვემოთ. ქვემოთ მოცემული სქემებიდან და ცხრილიდან ხედავთ, რომ მისი რეალურ დროში გამოყენება მარტივია gpu-ს გამოყენებით.\
<br />
Performance results was tested on GPU RTX 4090 (24GB) and CPU 13th Gen Intel(R) Core(TM) i9-13900K. \
Ubuntu 22.04.4 LTS \
Experements was done with different number of characters, audio durations and their infrence time on cpu and gpu and is given below. You can see from charts and table below, that it easy to use it in real time using gpu.

## CPU performance
<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th colspan="5" halign="left">inference time in seconds</th>
      <th colspan="5" halign="left">audio duration in seconds</th>
    </tr>
    <tr>
      <th></th>
      <th>mean</th>
      <th>quantile_0.01</th>
      <th>quantile_0.25</th>
      <th>quantile_0.75</th>
      <th>quantile_0.99</th>
      <th>mean</th>
      <th>quantile_0.01</th>
      <th>quantile_0.25</th>
      <th>quantile_0.75</th>
      <th>quantile_0.99</th>
    </tr>
    <tr>
      <th>number of characters</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>32</th>
      <td>0.453381</td>
      <td>0.389013</td>
      <td>0.414706</td>
      <td>0.487909</td>
      <td>0.604449</td>
      <td>3.929977</td>
      <td>3.552653</td>
      <td>3.877732</td>
      <td>3.970612</td>
      <td>4.237642</td>
    </tr>
    <tr>
      <th>64</th>
      <td>0.754833</td>
      <td>0.652958</td>
      <td>0.696219</td>
      <td>0.799385</td>
      <td>0.994115</td>
      <td>6.440054</td>
      <td>6.118458</td>
      <td>6.315828</td>
      <td>6.606077</td>
      <td>6.826667</td>
    </tr>
    <tr>
      <th>256</th>
      <td>2.451267</td>
      <td>2.225817</td>
      <td>2.357944</td>
      <td>2.518129</td>
      <td>2.726624</td>
      <td>20.833408</td>
      <td>20.143311</td>
      <td>20.654150</td>
      <td>20.921179</td>
      <td>22.198277</td>
    </tr>
    <tr>
      <th>512</th>
      <td>4.659979</td>
      <td>4.416153</td>
      <td>4.552752</td>
      <td>4.736746</td>
      <td>5.030857</td>
      <td>38.833749</td>
      <td>37.918186</td>
      <td>38.591565</td>
      <td>39.102404</td>
      <td>39.601633</td>
    </tr>
  </tbody>
</table>

## GPU performance
<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th colspan="5" halign="left">inference time in seconds</th>
      <th colspan="5" halign="left">audio duration in seconds</th>
    </tr>
    <tr>
      <th></th>
      <th>mean</th>
      <th>quantile_0.01</th>
      <th>quantile_0.25</th>
      <th>quantile_0.75</th>
      <th>quantile_0.99</th>
      <th>mean</th>
      <th>quantile_0.01</th>
      <th>quantile_0.25</th>
      <th>quantile_0.75</th>
      <th>quantile_0.99</th>
    </tr>
    <tr>
      <th>number of characters</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>32</th>
      <td>0.017791</td>
      <td>0.015188</td>
      <td>0.016126</td>
      <td>0.017405</td>
      <td>0.025912</td>
      <td>3.930906</td>
      <td>3.656446</td>
      <td>3.840000</td>
      <td>3.996735</td>
      <td>4.412952</td>
    </tr>
    <tr>
      <th>64</th>
      <td>0.024347</td>
      <td>0.020326</td>
      <td>0.021126</td>
      <td>0.028447</td>
      <td>0.031071</td>
      <td>6.429373</td>
      <td>6.048798</td>
      <td>6.280998</td>
      <td>6.524807</td>
      <td>6.958324</td>
    </tr>
    <tr>
      <th>256</th>
      <td>0.071052</td>
      <td>0.060597</td>
      <td>0.062858</td>
      <td>0.076386</td>
      <td>0.079714</td>
      <td>20.812394</td>
      <td>20.199851</td>
      <td>20.569977</td>
      <td>21.028571</td>
      <td>21.525943</td>
    </tr>
    <tr>
      <th>512</th>
      <td>0.130159</td>
      <td>0.118664</td>
      <td>0.121434</td>
      <td>0.141063</td>
      <td>0.144757</td>
      <td>38.956815</td>
      <td>37.952784</td>
      <td>38.588662</td>
      <td>39.267846</td>
      <td>40.183757</td>
    </tr>
  </tbody>
</table>

# კონტაქტები / Contacts
თუ გაინტერესებთ ქართული TTS მოდელის ტესტირება, გთხოვთ, ნუ მოგერიდებათ მომწეროთ ელექტრონული ფოსტით: icegas555@gmail.com <br /> 
ჩვენ ასევე შეგვიძლია დავლიოთ ფინჯანი ყავა და ვიმსჯელოთ პოტენციურ თანამშრომლობაზე, თუ დაინტერესდებით\
<br />
If you're intersted in testing Georgian TTS model, please don't hesistate to contact me via email: icegas555@gmail.com <br /> 
We can also drink a cup of coffe and discuss potential collaboration if you're intersted. 
# Other languages
If you need to create TTS system using different language, i'd like to help, please contact me directly by email.
