# tests senarios

## Cpu stress 

      @ pass first phase
          send packet with size = 1
      @ pass second phase
          send packet with size = 2
     @ pass third phase 
          send packet with size = 3 
      @ pass forth phase 
          send packet with size = 4 
      @ pass fifth phase 
          send packet with size = 5 
      @ failing any phase 
          send packet with size = 9 
      @ test finish 
          send packet with size = 1 
          send packet with size = 1 
          send packet with size = 1

      
## Mem stress 	

     @ start of test 
        send packet with size = 1
     @ pass bytes  
        send packet with size = 2
     @ pass int  
        send packet with size = 3
     @ pass short  
        send packet with size = 4
     @ error reading 
        send packet with size = 9
     @ test finish 
        send packet with size = 7
        send packet with size = 7
        send packet with size = 7
      
## IRQ_timer

    @configuring the timers and start count down 
        send packet size = 1

    @received interrupt correctly  test pass
        send packet size = 5

    @ timeout                       test fail
        send packet size = 9

    @ end test 
        send packet size = 3
        send packet size = 3
        send packet size = 3

## timer0_oneshot

    @configuring the timers and start count down 
        send packet size = 1

    @timer  updated correctly 
        send packet size = 5

    @timer reach 0
        send packet size = 7

    @ timer updated incorrectly
        send packet size = 9

    @ end test 
        send packet size = 3
        send packet size = 3
        send packet size = 3
        
## IRQ_uart 

    @request sending data through the uart 
        send packet size = 1

    @received interrupt correctly  test pass
        send packet size = 5

    @ timeout                       test fail
        send packet size = 9

    @ end test 
        send packet size = 3
        send packet size = 3
        send packet size = 3
        
## timer0_periodic 

    @configuring the timers and start count down 
        send packet size = 1

    @timer rollover  test pass
        send packet size = 5

    @ timer has not rollover
        send packet size = 9

    @ end test 
        send packet size = 3
        send packet size = 3
        send packet size = 3
