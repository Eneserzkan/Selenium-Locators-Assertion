# Selenium-Locators-Assertion
It is about basic selenium automation for using locators and assertion.


from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.chrome.service import Service
import time

driver = webdriver.Chrome(executable_path="C:\\Users\\enes.erozkan\\Desktop\\driver\\chromedriver.exe")
driver.maximize_window()

url = "https://www.lcwaikiki.com/tr-TR/TR"
driver.get(url)

driver.get("https://www.lcwaikiki.com/tr-TR/TR/lp/32-33-kadin")
time.sleep(2)

driver.find_element(By.XPATH, "//*[@id='landingPageContainer']/div/div[1]/div[1]/a[2]").click()
time.sleep(1)

driver.find_element(By.CLASS_NAME, "product-card__title").click()
driver.find_element(By.XPATH, "//*[@id='cookieseal-banner']/div/button[2]").click()





#time.sleep(2)
#time.sleep(5)
#driver.quit()
