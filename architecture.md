# Waffle

## Component UML

> Waffle is a Discord bot that manages Discord servers using Ollama for LLM inference and MCP for tool execution.

![Component UML](https://img.plantuml.biz/plantuml/svg/TL6z2i8m4DxlAOxkxGCK2HKTT10xL1mbjbSef4b9qa74TpTf6unICoJ7ztDtV2cCvTgElG2eLJyeITBYbRUje0X8zfsfbMvmMnuJt6n4TzTSFnX3Rd3X70KWLKDusfNu17IdavPqosl2GrMLNkoucwydUcM0uvEWMp1N_bElhHCv_KhUELrXCgPhpRyXJDbldrSSq5a8tlDuCW3a5qCwzzObl_dnmAmFG9QnJmv1D0vE5qTPa6pSlxm1)

<!-- ```plantuml
@startuml

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
