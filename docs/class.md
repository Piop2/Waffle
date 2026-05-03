# Class UML

## Waffle Class Structure

![Class UML](https://img.plantuml.biz/plantuml/svg/bPB1QWCX48RlynJ3df90X5nBieJc7EYjPxDgAwWJr9BqxJkwkfIq5EfXmPb__lbcrcFACkOFx-3TAerU-ukE2RBDJkEhDCPf09YSJ0cVAUD-hsoQA2fn_Hn729GrEcqoaYbvG3ucaiSkq_UCrbyfPfp8UnbKggBwkR3ZOOaBDbW98TQWWy9YtJkVwEtFpfp_P-Tb8YvTBG1yMJ_LV3cCyeEahwHnEQj3MGev9xtiM3nMPf02LWNGC6PLAQvbXnOGi-htqS-dbsO2C3V7pLRHBMp7kl37M1C_Xh_PbDyux0QadXjsGco6kaI08mFmS_W2)

<!-- ```plantuml
@startuml
hide members
title Waffle

class Bot <<discord.py>>
note left of Bot
    from discord.ext import commands
    
    bot = commands.Bot(...)
end note

class Cog <<discord.py>>
note left of Cog
    from discord.ext import commands
    
    class BotCog(commands.Cog):
        ...
end note

class Waffle

class Client <<ollama>>
note bottom of Client
import ollama

client = ollama.Client(...)
end note

class MCPClient

Waffle *-down-> Bot
Waffle *-down-> Client
Waffle *-down-> MCPClient

Bot "1" o-down-> "1..*" Cog

@enduml
``` -->

<!-- ## Waffle MCP Server Class Structure -->
