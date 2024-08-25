自动按定时登录serv00的账号，并按时启动服务器的节点。
-------------------------------------------------------------------------------------------------
WebLogin配置信息                                                                        
添加以下 Secrets：                                                                             
WebLogin中ACCOUNTSWEB_JSON: 包含账号信息的 JSON 数据。例如：

 
   [   
    {"username": "serv00的账号", "password": "serv00的密码", "panel": "panel6.serv00.com"},            
  
    {"username": "ct8的账号", "password": "ct8的密码", "panel": "panel.ct8.pl"},             
  
    {"username": "user2", "password": "password2", "panel": "panel6.serv00.com"}                              
   ]                                                         

                                                                                                   

TELEGRAM_BOT_TOKEN: 你的 Telegram Bot 的 API Token。
TELEGRAM_CHAT_ID: 你的 Telegram Chat ID。

----------------------------------------------------------------------------------------------------
RecoveryCommand配置信息                                  
修改 ACCOUNTS_JSON                                                     


[   
      {   
        "host": "example1.com",
        "port": 22,
        "username": "user1",
        "password": "password1",
        "cron": "cd ~/domains/$USER.serv00.net/vless && ./check_vless.sh"
      },     
     
      {
        "host": "example2.com",
        "port": 22,
        "username": "user2",
        "password": "password2"
        // 没有cron参数，使用默认命令
      }
]

                                                                                            
TELEGRAM_BOT_TOKEN: 你的 Telegram Bot 的 API Token。    
TELEGRAM_CHAT_ID: 你的 Telegram Chat ID。                                                        
 
