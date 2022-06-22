<p style="font-size:14px" align="right">
Join our telegram <a href="https://t.me/berkcak" target="_blank"><img src="https://user-images.githubusercontent.com/50621007/168689534-796f181e-3e4c-43a5-8183-9888fc92cfa7.png" width="30"/></a>
Visit our website <a href="https://minima.global//" target="_blank"><img src="https://user-images.githubusercontent.com/50621007/168689709-7e537ca6-b6b8-4adc-9bd0-186ea4ea4aed.png" width="30"/></a>
</p>



# MinimaTR-script-kurulum


 <h1 align=“center”>Minima Node Kurulum Türkçe Rehberi </h1> 
<p>https://aws.amazon.com/  üzerinden  üyelik oluşturarak 12 aylık ücretsiz makinenizi açabilirsiniz, ve sistem gereksinimleri çok düşük, herkes kolayca kurabilir</p>

![image](https://user-images.githubusercontent.com/101149671/171995342-a449138d-b3c7-493b-98d7-2f3e6e67feed.png)

# Üyelik oluşturduktan sonra;

![image](https://user-images.githubusercontent.com/101149671/171995425-5f951569-3312-42c9-a43e-7a6f39941d04.png)

# Name kısmına istediğiniz bir isim yazıyorsunuz ve aşağıdan ubuntu (20.04) seçiyorsunuz.

![image](https://user-images.githubusercontent.com/101149671/171995434-dd6b4c9a-ff77-43a7-8ae7-b0cb367fb311.png)

# Create new key pair yazan yere tıklayıp bir isim veriyoruz ve kaydediyoruz bir dosya indirecek: 

<p> Ardından kurulumda başka hiçbir şeyi değiştirmeden sağ altta bulunan launch instance kısmına tıklayıp makine kurulumunu bitiriyoruz.<p>

![image](https://user-images.githubusercontent.com/101149671/171995488-d5c0e279-2c62-4f42-a1fd-5267af362746.png)

# Karşınıza böyle bir sayfa çıkacak sol üstte aws yazısının altında benim çizdiğim çizgilerin orada 3 çizgi olacak oraya basıp instances bölümüne giriyoruz:

![image](https://user-images.githubusercontent.com/101149671/171996368-de9e05c2-b4c3-46a8-aceb-ac254d2a88f2.png)


#  Instance state kısmı running olana kadar bekliyoruz. Ardından okla gösterdiğim ID kısmına tıklayıp giriyoruz:

![image](https://user-images.githubusercontent.com/101149671/171996371-b20929ab-611b-41f1-831b-513f7f62c656.png)

# Okla gösterdiğim connect butonuna tıklıyoruz. Açılan sayfada name kısmına bir isim girin ve sağ altta bulunan connect butonuna basın. Yeni bir pencere açılacak.

![image](https://user-images.githubusercontent.com/101149671/171996374-33bf9cc6-52fd-4fa8-b82e-6cf69a4fcd10.png)

# Bu komutu ctrl+v ile yapıştırıp enterlıyoruz :
```
wget -O minima_setup.sh https://raw.githubusercontent.com/minima-global/Minima/master/scripts/minima_setup.sh && chmod +x minima_setup.sh && sudo ./minima_setup.sh -r 9002 -p 9001
```
![image](https://user-images.githubusercontent.com/101149671/171995567-ef262db0-a043-43ca-b535-644013771b21.png)

#  Arkada kurulum devam ederken vereceğim linke girip üyelik oluşturuyoruz daha sonrasında hesabımıza giriş yapıyoruz:
Girdikten sonra en üstte bulunan Incentive IDyi kopyalıyoruz hazır dursun; 

[Link](https://incentive.minima.global/account/register?inviteCode=GEEASBDR)

# Kırmızı ile işaretlediğim yerden önceki komutları gördüğünüzde kurulumun bittiğini anlıyoruz ve CTRL + C tuşlarına basıyoruz.

![image](https://user-images.githubusercontent.com/101149671/171995728-75b89fcf-300d-417c-bb7b-49486039d45d.png)

Şimdi vereceğim koddaki XXXXX yazan kısma yukarıda üyelik açıp aldığınız kendi Incentive ID nizi yazmalısınız tekrardan siyah ekrana dönüp CTRL + V ile yapıştırıyoruz ve enterlıyoruz biraz bekledikten sonra kurulum tamamdır, komut:
```
curl 127.0.0.1:9002/incentivecash+uid: XXXXXXXXXXX
```

# Fotoğrafta last ping yazan yerden nodunuzun çalışıp çalışmadığını kontrol edebilirsiniz:

![image](https://user-images.githubusercontent.com/101149671/171996301-497a15bf-64bb-404b-a19f-e79d50752f41.png)

## Faydalı komutlar

```
ctrl-c : Minima loglarından çıkar (Minima arka planda çalışmaya devam eder)
```

```
journalctl -u minima_9001 -f : Minima günlüklerini göster
```

```
sudo ps -fC java : Çalışan tüm Java işlemlerini gösterir
```

```
sudo apt install curl : minima ile etkileşim kurmak için curl komutlarını kullanmanıza izin verir
```

```
Then y (for Yes)
```

```
sudo apt install jq : allows you to use jq to make the output look readable
```

 ```
Then y (for Yes)
```

```
Stopping/starting Minima (Servis minima.service olarak adlandırılmalıdır)
```

```
sudo systemctl stop minima_9001 - Minima hizmetini durdur
```

```
sudo systemctl disable minima_9001 - Minima hizmetini devre dışı bırakın
```

```
sudo systemctl enable minima_9001 - Minima hizmetini etkinleştirin
```

```
sudo systemctl start minima_9001 - Minima hizmetini başlatın
```


### Interacting with Minima


```
curl 127.0.0.1:9002/status | jq - Minima'nın durumunu gösterir
```

```
curl 127.0.0.1:9002/incentivecash | jq - teşvik nakit bakiyenizi gösterir
```

```
curl 127.0.0.1:9002/help | jq - komutların tam listesini gösterir
```

###Forumda yazmış olduğum flood: https://forum.rues.info/index.php?threads/minima-node-kurulumu-oeduellue.399/
> Sormak istediğiniz bir şey varsa yazının başında bulunan telegram simgesine tıklayarak bana ulaşabilirsiniz
