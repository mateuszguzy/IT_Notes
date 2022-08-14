


  
Is a software for automated web browsing. It cooperates with major web browsers and is used to automate tasks done with use of them.  
  
At the beginning local host needs a driver to particular browser it's gonna use.  
For Firefox it's Geckodriver, for Chrome - Chromedriver.  
  
Setting browser driver looks like below:  
  

```python
from selenium import webdriver  
  
firefox\_driver\_path = "/driver/file/path"  
driver = webdriver.Chrome(executable\_path="firefox\_driver\_path")  
# to open certain web page in a browser  
driver.get("www.example.com")  
# to close single tab of the browers  
driver.close()  
# to close entire browser  
driver.quit()
```
