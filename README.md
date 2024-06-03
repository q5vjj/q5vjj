import requests
import random,threading
from colorama import *
RJJF = '\033[1;34m' #ازرق
RJJF_ = '\033[1;31m' # احمر
RJJFF = '\033[1;35m' # بنفسج
RJ_ = '\033[1;32m' #اخضر
RJJ = '\033[1;34m' #ازرق فاتح
RJ__ = '\033[1;33m' #اصفر

print("""\033[1;34m
--  /$$$$$$$     /$$$$$    /$$$$$ /$$$$$$$$
-- | $$__  $$   |__  $$   |__  $$| $$_____/
-- | $$  \ $$      | $$      | $$| $$      
-- | $$$$$$$/      | $$      | $$| $$$$$   
-- | $$__  $$ /$$  | $$ /$$  | $$| $$__/   
-- | $$  \ $$| $$  | $$| $$  | $$| $$      
-- | $$  | $$|  $$$$$$/|  $$$$$$/| $$      
-- |__/  |__/ \______/  \______/ |__/      
""")
rt = requests.session()
ers = 'qwertyuiopasdfghjklzxcvbnm1234567890'
id = input(RJJFF+" જ⁀➴ Enter ID Your •.• ")
token = input(RJ__+" જ⁀➴ Enter Token bot •.• ")
print('')
headers = {"user-agent": "Mozilla/5.0 (Linux; Android 11; vivo 1904; RMX2142 Build/RP1A.128603.007; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/113.0.2237.146 Mobile Safari/537.36 swan-mibrowser"}
def vip():
	while True:
	 user1 = str("".join(random.choice(ers)for x in range(5)))
	 username = user1
	 rr = requests.get(f"https://www.tiktok.com/@{username}", headers=headers).text
	 if 'nickname' in rr:
	         print(RJJF_ + f'「 ❎ 』 ɴᴏ ᴀᴠᴀɪʟᴀʙʟᴇ {username} ')
	 else:
	 	print(RJ_+ f' 「 ✅ 』 ʏᴇs ᴀᴠᴀɪʟᴀʙʟᴇ {username}');requests.get(f"https://api.telegram.org/bot{token}/sendMessage?chat_id={id}&text= 「 ✅ 』 ʏᴇs ᴀᴠᴀɪʟᴀʙʟᴇ ~> :\n [ {username} ]\n DVE : @R_J_J_F • @RJJF1")
thread = []
for i in range(5):
    thread1 = threading.Thread(target=vip)
    thread1.start()
    thread.append(thread1)   	 	
vip()
