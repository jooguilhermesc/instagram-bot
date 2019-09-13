from selenium import webdriver
from selenium.webdriver.common.keys import Keys
from time import sleep, strftime
from random import randint
import pandas as pd

'''
PLX BE SURE U R ALREADY READ "READ ME" BEFORE STARTS TO USE THIS CODE

POR FAVOR TENHA CERTEZA DE TER LIDO O "READ ME" ANTES DE COMEÇAR A USAR ESSE CÓDIGO
'''

'''
[ENGLISH COMENTS]
This step of this project is where you set the website that you wish acess, and set the chromedriver path.
I'm linux user, so I used just "chromedriver" but if you're a Windows user, probabily you'll need use "chromedriver.exe"

[COMENTÁRIO EM PORTUGUÊS]
Nesta etapa do projeto você define o site que deseja acessa e define o caminho do chromedriver.
Eu sou um usuário linux, então eu usei "chromedriver", mas se você é um usuário Windows, provavelmente terá de usar "chromedriver.exe"
'''
chromedriver_path = '/home/joao/Downloads/chromedriver' # Change this to your own chromedriver path!
webdriver = webdriver.Chrome(executable_path=chromedriver_path)
sleep(2) #This is important because some websites don't allow make a lot request in a short time period 
webdriver.get('https://www.instagram.com/accounts/login/?source=auth_switcher')
sleep(3) #Isso é importante porque alguns sites não permitem fazer muitas requisições de acesso em um curto período de tempo


'''
[ENGLISH COMENT]
At this point you'll insert your credentials to acess Instagram plataform 

[COMENTÁRIO EM PORTUGUÊS]
Nessa etapa você vai vai inserir suas credenciias para acessar o Instagram
'''
username = webdriver.find_element_by_name('username')
username.send_keys('CLEAR_THIS_AND_INSERT_HERE_YOUR_USERNAME[LIMPE_ISSO_E_INSIRA_SEU_USERNAME]')
password = webdriver.find_element_by_name('password')
password.send_keys('CLEAR_THIS_AND_INSERT_HERE_YOUR_PASSWORD[LIMPE_ISSO_E_INSIRA_SUA_SENHA]')

button_login = webdriver.find_element_by_css_selector('#react-root > section > main > div > article > div > div:nth-child(1) > div > form > div:nth-child(4) > button')
button_login.click()
sleep(3)

hashtag_list = ['pagode','sertanejo','forró'] #INSERT HERE SOME HASTAGS OF YOUR INTEREST (INSIRA AQUI ALGUMAS HASTAGS DO SEU INTERESSE) 

prev_user_list = [] #THIS OPTION IS ONLY USED WHEN YOU'RE TRYING THIS FOR THE FIRST TIME (ESSA OPÇÃO SÓ É UTILIZADA SE VOCÊ ESTIVER FAZENDO ISSO PELA PRIMEIRA VEZ)


new_followed = []
tag = -1
followed = 0
likes = 0
comments = 0

for hashtag in hashtag_list:
    tag += 1
    webdriver.get('https://www.instagram.com/explore/tags/' + hashtag_list[tag] + '/')
    sleep(5)
    first_thumbnail = webdriver.find_element_by_xpath(
        '//*[@id="react-root"]/section/main/article/div[1]/div/div/div[1]/div[1]/a/div')

    first_thumbnail.click()
    sleep(randint(1, 2))

    while followed < 2:
        username = str(webdriver.find_element_by_css_selector(
            'body > div._2dDPU.vCf6V > div.zZYga > div > article > header > div.o-MQd > div.PQo_0 > div.e1e1d > h2 > a').text)

        if username not in prev_user_list:
            webdriver.find_element_by_xpath('/html/body/div[3]/div[2]/div/article/header/div[2]/div[1]/div[2]').click()
            followed += 1
            sleep(1)
            webdriver.find_element_by_xpath('/html/body/div[3]/div[2]/div/article/div[2]/section[1]/span[1]/button').click()
            likes += 1
            sleep(1)
            sleep(5)

        elif username in prev_user_list:
            try:
                webdriver.find_element_by_xpath('/html/body/div[3]/div[1]/div/div/a').click()
            except:
                print('ERRO')
                break

        prev_user_list.append(username)
