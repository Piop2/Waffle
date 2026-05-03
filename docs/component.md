# Component UML

![Component UML](https://img.plantuml.biz/plantuml/svg/TL7B2eCm4BplLopUzGD4n68FBLJgGUcnf1eX41D9ug6K_diJ7srQR0x9xipiWqcc3L5cx3aOPZZ52-awJcFCPJz8GON1kZW1DEzq5dX0i6UwaQh5NNaCC4aukocYxccAHEF2MGf0o9PYaPVu0BI72KDLHngAXwegdTXoLnTFzCO0omUhRi5i-4-zjOvNwLPobTErJiPmg_atX67ws-Vf6tJcdFJ4dmm0SQsfYbtfuj_yE63Mhq0KfHyVLj4uM9rlPKP5Q__i1G00)

<!-- ```plantuml
@startuml
title Waffle: Component UML

component Waffle
component "Discord API" <<library>> as DiscordAPI

node MCP {
    interface HTTP as MCP_HTTP
    component "Discord MCP" as MCP_DiscordMCP
    component "Discord API" <<library>> as MCP_DiscordAPI
    
    MCP_HTTP - MCP_DiscordMCP
    MCP_DiscordMCP -> MCP_DiscordAPI
}

component Ollama <<library>>


:User: -> Waffle
Waffle -> Ollama
Waffle ..> MCP_HTTP
Waffle -up-> DiscordAPI

@enduml
``` -->
