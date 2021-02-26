Unable-to-load-the-service-index-for-source-https-api.nuget.org-v3-index.json-2054

Yukarıda alınan hata ile .Net uygulamasında docker build ederken çok kez karşılaştım. 
Hatanın çözümü: 
  C:\ProgramData\Docker\config klasöründeki daemon.json dosyasının içine  "dns": ["8.8.8.8"] yazmak 
  Benim daemon.json dosyam aşağıdaki gibi görünüyor:
  {
  "registry-mirrors": [],
  "insecure-registries": [],
  "debug": false,
  "experimental": false,
  "dns": ["8.8.8.8"]
 }
