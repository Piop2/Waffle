# Activity Diagram

![Activity Diagram](https://img.plantuml.biz/plantuml/svg/hLLDZzem4Br7od-O8nog7dg3gYnTkXA7eksoFLJQYzSPY8MnezY1NObpVq1_Odz99tP2ljcYDeUGn3FpPjvxDZV6ijHcUna6LbY9i126wpI2tpz_mMTjtUzy2VUfvcYCK5kua_eO1c5mAaFNc1umFOM1gnK6a-y6Kp2e8WCCzfJ6jlYaZiB6y4mbzwYiq6hgYX06PKuUaACuLF1ue20N8JOm-kepCChpPsEmCIeOhVGu382koNAhT8fJ_sQiJi80fK4O_K1JnAIO8BF-sUNSqnS_LDdYj5gjdaxpvQcMjQQfWFBsYUqFz_ESuszZv3i2DubMfaJmlS0n5aJuQ9tnl8jD9cVmdjPiAj30H_Wm1c5gKxxx13HEKSBVSsuUjPR0cPHTNbn37PMQizWyFP5CNMGX1vedDFS1etwSorYU2wOuIi0Nv5bXWFgwrwsBtLPoWEgAsEOt1rqJsmtSdRMBUyPfEE0jA0TNCJiCv08No4M4eF35klY1kFwlFGIS2_Vwhjl_jHwiNmq_NkvsSeUMnqCJJhuuHs3VUhFDLSaJcKWOQsQ-lQutgBULRfLgkV6HcHtSqaQMQDi4NMLhBtPUZHVL1bHllkLRwa5B-SpuxhobkfEu1lg5BbZD37gpcISrIkdWJ6c_KBkOZlzAd8jEzX1l-REX86GgQdDVuPHIViimGq0wHrzd_yba9Pjd7Lfff9FO_8FG2sJSYWCR5BXvWZNhry3ztHzhLvtLnA1y9Ow1nqmfhAjHGHT0nKyOtD0J_R__0G00)

<!-- ```plantuml
@startuml
title Discord → Bot → AI Processing Flow

|Discord Server|
start
:User sends a message\nwith bot mention;

|Bot|
:Receive Discord event;

if (Mentioned bot?) then (No)
    :Ignore;
    stop
else (Yes)
    repeat
        :Preprocess message;
        
        |AI|
        :Send prompt;
        
        |Bot|
        :Check response;
    repeat while (Successful? / retries < 3) is (No)
    -> Yes;
    
    if (Tool call?) then (No)
        |Discord Server|
        :Send tool plan message;
        
        if (Approved?) then (No)
            |Discord Server|
            :Cancel execution;
            stop
        
        else (Yes)
            |Bot|
            repeat
                :Preprocess tool message;
                
                |AI|
                repeat
                    :Send tool message;
                    :Decide next tool;
                    
                    |Bot|
                    :Check response;
                repeat while (Successful? / retries < 3) is (No)
                -> Yes;
                
                :Fetch tool;
                :Execute tool;
            repeat while (Next tool exists?) is (Yes)
            -> No;
            
            :Task Complete;
            
            |Discord Server|
            :Send task complete message;
            
            if (Rollback?) then (Yes)
                |Bot|
                :Fetch used tools\n(reverse order);
                
                repeat
                    :Fetch next tool;
                    :Execute tool undo;
                repeat while (Queue empty?) is (No)
                -> Yes;
                
                :Rollback complete;
            endif
            
            |Discord Server|
            :Deactivate message;
            stop
            
        endif
    
    else (No)
        |Discord Server|
        :Send reply to channel;
        stop
    endif
endif

@enduml
``` -->