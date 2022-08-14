


  
![images/1324-1.png](images/1324-1.png)  
  
  
  
  
![images/1324-2.png](images/1324-2.png)  
  
  
graphene-django  
django-filters  
  
![images/1324-3.png](images/1324-3.png)  
  
![images/1324-4.png](images/1324-4.png)  
  
![images/1324-5.png](images/1324-5.png)  
  
  
  
  
  
  
SENDGRID\_SOURCE\_EMAIL=mateuszguzy6@gmail.com  
SENDGRID\_API\_KEY=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  
  
  
curl --request POST \  
 --url <https://api.sendgrid.com/v3/mail/send> \  
 --header 'Authorization: Bearer SG.oMX-HyDeTu6yC68GuJIM0w.EDwRCg\_M8uB8sHN0t5e7JjFCbsFOlKfU3cot0wYuc0c' \  
 --header 'Content-Type: application/json' \  
 --data '{"personalizations": [{"to": [{"email": "mateusz.guzy@stxnext.pl"}]}],"from": {"email": "onedevhub@gmail.com"},"subject": "Hello, World!","content": [{"type": "text/plain", "value": "Heya!"}]}'  
  
  
  
  
  
  
