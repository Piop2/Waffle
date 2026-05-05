# Class Diagram

![Class UML](https://img.plantuml.biz/plantuml/svg/VLHBYzim4BxhLmm-9MrYw5LaJThjfT1IA5jw224ejfoOofQHnZJBDl-zeuSVyNRZapJVlBvlnjfQ50QxMZ6iK4du9SfIIGwFIbWBFxzzPOor8lyjJXAAokRQ5B3PV0wdj7tECdXXG5_k0v97LSa64n0MejCXcBnJer62aYM2Bl-7bqRNGvcgRhL1cC2naBl3GmGMQPekFI2RmXTWLyP2Du5CR70D1wNgGmZdyBsLpSSlFO9QgyDHNpWyqUcJlhWaFMzDhg8YsY7c3kNWy2RZrx0d7FD7lfF6Rla6u1xVsFj8sD6od1JDSMVHhBp7Vipz7fo7JqaZ5qg9ev8HEKbSDAAcNQ38PH0cGhQLkLsGJLKMToxxdfhmL4rrEdkkiHVEiOyh98rLe3RGMPALZsriU_bJtuwtUV6e_4D2tIMhmLP8cvkgnKetSuXk_hoCvSh0Zlfqo20NAmIAKR2eLc0Lj8e6UP5vXtAYp9MTgqA6i5hYMHUMtKpO8PoxJ3v7uXWaNi5mdtG_DRV2a2DAOycw6mYz3ATPijKjy2hh3CVdTjg5-wwhGQwm3ucHs1aNFrQzbtYUzFgcm3-axHJ2vYaRfUxoN5hQpEEuL2w8jYpUkgRGxYTrfONQzHFOJqSG4_U3O2p-x-kkNV_DvkzBVDdu-0Z0kj1_cdLs-ry2X_miHl_XRO3aGmAwZt6N_grWmxA7FsxkcQRlWdFmv3nk5gJPb0Y7C0DYiYKnwL7-1m00)

<!-- ```plantuml
@startuml
title Waffle: Class UML


package discord <<Discord.py>> {
    class "Client" as Discord_Client
    note left of Discord_Client
    from discord import Client
    
    client = Client(...)
    end note
}

class Waffle {
    - _llm_client: OpenAI
    - _tool_box: ToolBox
}

package openai <<OpenAI>> {
    class "Client" as OpenAI_Client
    note left of OpenAI_Client
    from openai import OpenAI
    
    client = OpenAI(...)
    end note
}

class ToolBox {
    - _tools: dict[str, Tool]
    
    + tool(...): Callable
    + get(name: str): Tool
    + specs(): list[dict]
}
note right of ToolBox::tool
    decorator usage:
    
    @tool_box.tool(
        name="...",
        description="...",
        ...
    )
    def tool(): ...
end note

dataclass Tool {
    + spec: dict
    + execute: Callable
}
hide Tool methods
note left of Tool::spec
    "name": str
    "description": str
    "parameters": [
        {
            "name": str,
            "description": str,
            "type": str
        }, ...
    ]
    "return": {
        "description": str,
        "type": str
    }
end note

dataclass ToolResult <T> {
    + success: bool
    + data: T
    + undo: Optional[Callable]
}
hide ToolResult methods


Waffle -up-|> Discord_Client
Waffle::llm_client -down-> OpenAI_Client : chat
Waffle::_tool_box "1" o-down-> "1" ToolBox

ToolBox::_tools "1" o-down-> "1..*" Tool

Tool::execute .> ToolResult : return


@enduml
``` -->
