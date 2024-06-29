# ქართული ტექსტის სიტყვის სინთეზი / Georgian-TTS 
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
      <td>0.320311</td>
      <td>0.146636</td>
      <td>0.157055</td>
      <td>0.168328</td>
      <td>4.103730</td>
      <td>3.929861</td>
      <td>3.657143</td>
      <td>3.851610</td>
      <td>3.982222</td>
      <td>4.458928</td>
    </tr>
    <tr>
      <th>64</th>
      <td>0.675573</td>
      <td>0.199406</td>
      <td>0.210842</td>
      <td>0.223745</td>
      <td>5.381177</td>
      <td>6.401858</td>
      <td>6.141678</td>
      <td>6.292608</td>
      <td>6.504490</td>
      <td>6.711263</td>
    </tr>
    <tr>
      <th>256</th>
      <td>10.147135</td>
      <td>0.590234</td>
      <td>0.629524</td>
      <td>14.319341</td>
      <td>14.778163</td>
      <td>20.833988</td>
      <td>20.211926</td>
      <td>20.607710</td>
      <td>21.008254</td>
      <td>21.584922</td>
    </tr>
    <tr>
      <th>512</th>
      <td>21.829358</td>
      <td>1.131615</td>
      <td>26.419551</td>
      <td>27.857851</td>
      <td>28.568445</td>
      <td>38.878563</td>
      <td>38.056345</td>
      <td>38.553832</td>
      <td>39.154649</td>
      <td>39.882014</td>
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
      <td>0.024355</td>
      <td>0.014626</td>
      <td>0.015937</td>
      <td>0.016883</td>
      <td>0.407303</td>
      <td>3.962485</td>
      <td>3.691973</td>
      <td>3.866122</td>
      <td>4.017052</td>
      <td>4.435476</td>
    </tr>
    <tr>
      <th>64</th>
      <td>0.032140</td>
      <td>0.020465</td>
      <td>0.021048</td>
      <td>0.021985</td>
      <td>0.536277</td>
      <td>6.417995</td>
      <td>6.094658</td>
      <td>6.269388</td>
      <td>6.548027</td>
      <td>6.898068</td>
    </tr>
    <tr>
      <th>256</th>
      <td>0.344305</td>
      <td>0.058727</td>
      <td>0.060569</td>
      <td>0.064237</td>
      <td>1.504808</td>
      <td>20.838980</td>
      <td>20.233520</td>
      <td>20.642540</td>
      <td>21.066304</td>
      <td>21.397653</td>
    </tr>
    <tr>
      <th>512</th>
      <td>1.085138</td>
      <td>0.115699</td>
      <td>0.118506</td>
      <td>2.785288</td>
      <td>2.876193</td>
      <td>38.943695</td>
      <td>37.695971</td>
      <td>38.542222</td>
      <td>39.256236</td>
      <td>39.999390</td>
    </tr>
  </tbody>
</table>
<br />
დასკვნის დრო დამოკიდებულია შეყვანის ექსპონენციალურობაზე, დამუშავებისთვის სჯობს ტექსტი 64-128 სიმბოლოთი თითოეული ნაწილებზე გადაფურთხოთ. <br />
Inference time depends on input exponentialy, it's better to spit text on chunks 64-128 characters each for processing.

# კონტაქტები / Contacts
თუ გაინტერესებთ ქართული TTS მოდელის ტესტირება, გთხოვთ, ნუ მოგერიდებათ მომწეროთ ელექტრონული ფოსტით: icegas555@gmail.com <br /> 
ჩვენ ასევე შეგვიძლია დავლიოთ ფინჯანი ყავა და ვიმსჯელოთ პოტენციურ თანამშრომლობაზე, თუ დაინტერესდებით\
<br />
If you're intersted in testing Georgian TTS model, please don't hesistate to contact me via email: icegas555@gmail.com <br /> 
We can also drink a cup of coffe and discuss potential collaboration if you're intersted. 
# Other languages
If you need to create TTS system using different language, i'd like to help, please contact me directly by email.
