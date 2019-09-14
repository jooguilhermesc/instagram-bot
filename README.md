# instagram-bot
An instagram bot that follows and like profiles searching for hastags. 

This tool was developed as a part of my project "music battle", this bot have a simple function search for some hastags that I want and follow the main profiles related to that subject.

Still have some issues in this project and I'm working to fix them. 

The main work at this project is to select the right css selector or xpath to aplly in the code. Sometimes I had problems using xpath when I was wishing use click() function, with css selectors works better, so sometimes you'll need change some selectors (don't ask me why this is fuckin' JS, man... kkkkkk) and is necessary to pay attention in elements that you choose.

And, to be honest I used a lot of this text: https://towardsdatascience.com/increase-your-instagram-followers-with-a-simple-python-bot-fde048dce20d

Even that I needed to change a lot of thing, this texts helps me a lot.

1 - How to configure your enviroment to run this project?

step 1) Install selenium and pandas usind pip comand:
Here you can find more about selenium project: https://pypi.org/project/selenium/
Here you can find more about pandas project: https://pypi.org/project/pandas/

step 2) Download and set drive:
First you'll need to check what's the version of the browser that you're using. 

If you're using Chrome: You can just click on the options and look for "Help", then you choose "About Google Chrome".
If you're using Firefox: Is the same way of Chrome, but U choose "About Firefox".

Now you can download chromedriver for the version that you have installed on your machine here: https://chromedriver.chromium.org/downloads

And you can download geckodriver (firefox driver) with this link: https://github.com/mozilla/geckodriver/releases

step 3) set the path to driver in the code 

[VERSÃO EM PORTUGUÊS]

Um bot de instagram que segue e curte perfis procurando por hastags.

Esta ferramenta foi desenvolvida como uma parte do meu projeto "music battle", este bot tem a simples função de procurar por algumas hastags que eu quero monitorar e seguir os principais perfis relacionados ao assunto.

Ainda tem alguns problemas, mas estou consertando.

A principal parte do trabalho foi escolher o seletor ideal, porque algumas vezes o xpath funcionava com algumas coisas e outras vezes o css selector funcionava melhor, então é importante prestar atenção nesses detalhes. Outro ponto pra atentar é em relação ao elemento que você escolhe.
