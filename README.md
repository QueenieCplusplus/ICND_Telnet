# ICND Telnet
與遠端設備建立連線

相對於 console 控制埠（簡寫為 con 0），虛擬終端機通訊協定的簡寫為 vty 0~4 (全名為 virtual terminal)，它使得一設備可連線往返單一或多項遠端設備。

# 路由器設備的遠端連線

    (router)# <remote network equipment or hotst IP addr>
    
    (router)# show session
    //確認使否連線成功
    //會顯示所有已經遠端連線的session訊息
    //其中有*星號在前頭的session為最新連線，按下 enter 可回到此連線設定
    
    (router)# show user
    //檢視控制埠與遠端連線資訊集合

# 交換器設備的遠端連線

    (sw)# telnet <remote network equipment or host IP addr>
    
    (sw)# sh session
    //確認使否連線成功
    //會顯示所有已經遠端連線的session訊息
    //其中有*星號在前頭的session為最新連線，按下 enter 可回到此連線設定
    
    (sw)# sh user
    //檢視控制埠與遠端連線資訊集合
    
# sh session & sh user

這些在 UNIX 系統，指令為


        where

        who
        
        
範例：

         ~  ✗ who
        pintred  console  Jun 18 21:02 
        pintred  ttys000  Jun 18 21:04 


# 終止遠端連線

從設備端而言

        (router)# show user
        //確認要關閉哪個連線對象。

        (router)# clear line <連線編號>
        //從 console 方關閉來自遠端連線的使用者。

從主機而言
