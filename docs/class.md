# Class UML

![Class UML](https://img.plantuml.biz/plantuml/svg/VLJBRjim4BppAnOyEQqje5SXCTmcbm0fSadHWn4OZ4IvH6YH85U8WzJ_tkL3ZoYfTI9tPdTdXwGs7eN3xg0PAjGIVekcqRA4QosyXry_xnXZLbJFOY-XLhuoheRBovkqAkphUWrl3EYhOWA_ragso45uoAHT2aLIQr22bWs2QJx36sSEGnjriCOXJE3SAEpXAWEBeYWk8Y3REZPW9yQIcZJCE82niXMAzD_Jullj6Us9y5_f7-6eFDVFmXFf4-49E2VymHZzmnopl1Nia0A-96igt7fqoyXu76j_XS289UdiXDRYYGPFo5xYeXK7EbJA93YaPiXRMVa5nRJok0tL7qb47DMf_PyuQzPIbjZdrPBEHw1nq7cojHnbR09dzsIEHPGJOz4yQd_5IHrV3h5Q-iefYygqSuXsSNsHspLfEj8PaC4kLWiKes7PhJHLyYe7v55M7P81zx6TqDlUec7S_cH3eR8C5M8k3yfvT2xj9wgdOIiS4L4wJz7jCCZRi9eLMxu7FbITuVXgfoh2TreEDgLxm9t4peNyiUkvmlEYfucnBBqSM7LszNSzVwazM9kNThMUFOOCycySJCy8ctoD61lkKxhKSsPHV4baKh4XHVHh-WS0)

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

class Waffle

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
    + execute: Optional[Callable]
}
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


Waffle -up-|> Discord_Client
Waffle -down-> OpenAI_Client
Waffle "1" o-down-> "1" ToolBox

ToolBox::_tools "1" o-down-> "1..*" Tool


@enduml
``` -->
