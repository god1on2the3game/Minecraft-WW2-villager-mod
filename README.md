# Minecraft-WW2-villager-mod
{
  "format_version": 2,
  "header": {
    "name": "WWII Villager Addon",
    "description": "A World War II themed villager addon with military professions, custom items, and trades for Minecraft Bedrock Edition",
    "uuid": "550e8400-e29b-41d4-a716-446655440001",
    "version": [1, 0, 0],
    "min_engine_version": [1, 20, 0]
  },
  "modules": [
    {
      "description": "Behavior Pack",
      "type": "data",
      "uuid": "550e8400-e29b-41d4-a716-446655440002",
      "version": [1, 0, 0]
    },
    {
      "description": "Resource Pack",
      "type": "resources",
      "uuid": "550e8400-e29b-41d4-a716-446655440003",
      "version": [1, 0, 0]
    }
  ],
  "dependencies": [
    {
      "uuid": "1828161e-51eb-430f-bcc1-4b61143dfa12",
      "version": [1, 0, 0]
    }
  ]
}
{
  "format_version": 2,
  "header": {
    "name": "WWII Villager - Behavior Pack",
    "description": "Behavior pack for WWII villager addon",
    "uuid": "550e8400-e29b-41d4-a716-446655440004",
    "version": [1, 0, 0],
    "min_engine_version": [1, 20, 0]
  },
  "modules": [
    {
      "description": "Behavior Pack Module",
      "type": "data",
      "uuid": "550e8400-e29b-41d4-a716-446655440005",
      "version": [1, 0, 0]
    }
  ]
}
{
  "format_version": "1.20.0",
  "minecraft:entity": {
    "description": {
      "identifier": "wwiivillager:soldier_villager",
      "is_spawnable": true,
      "is_summonable": true,
      "is_experimental": false
    },
    "component_groups": {
      "wwiivillager:soldier_base": {
        "minecraft:type_family": {
          "family": ["villager", "mob", "human"]
        },
        "minecraft:health": {
          "value": 20,
          "max": 20
        },
        "minecraft:nameable": {
          "allow_name_tag_renaming": true
        },
        "minecraft:rideable": {
          "seat_count": 1,
          "interact_text": "action.interact.ride.horse",
          "seats": [
            {
              "position": [0.0, 0.0, 0.0],
              "rotate_rider_relative": false
            }
          ]
        }
      },
      "wwiivillager:soldier_equipment": {
        "minecraft:equipment": {
          "table": "loot_tables/entities/soldier_equipment.json"
        }
      },
      "wwiivillager:soldier_trades": {
        "minecraft:trade_table": {
          "table": "trading/soldier_trades.json"
        }
      }
    },
    "components": {
      "minecraft:type_family": {
        "family": ["villager", "mob", "human"]
      },
      "minecraft:health": {
        "value": 20,
        "max": 20
      },
      "minecraft:armor": {
        "slots": [
          {
            "slot": 0,
            "item": "wwiivillager:military_helmet"
          },
          {
            "slot": 1,
            "item": "wwiivillager:military_chest"
          },
          {
            "slot": 2,
            "item": "wwiivillager:military_legs"
          }
        ]
      },
      "minecraft:movement": {
        "value": 0.5
      },
      "minecraft:behavior.look_at_player": {
        "priority": 0,
        "range": 6.0
      },
      "minecraft:behavior.random_look_around": {
        "priority": 1
      },
      "minecraft:behavior.wander": {
        "priority": 2,
        "speed_multiplier": 0.6
      },
      "minecraft:behavior.panic": {
        "priority": 3
      },
      "minecraft:nameable": {
        "allow_name_tag_renaming": true
      },
      "minecraft:despawn": {
        "despawn_delay": 600
      }
    },
    "events": {
      "wwiivillager:soldier_spawn": {
        "add": {
          "component_groups": ["wwiivillager:soldier_base", "wwiivillager:soldier_equipment", "wwiivillager:soldier_trades"]
        }
      }
    }
  }
}
{
  "format_version": "1.20.0",
  "minecraft:entity": {
    "description": {
      "identifier": "wwiivillager:medic_villager",
      "is_spawnable": true,
      "is_summonable": true,
      "is_experimental": false
    },
    "component_groups": {
      "wwiivillager:medic_base": {
        "minecraft:type_family": {
          "family": ["villager", "mob", "human"]
        },
        "minecraft:health": {
          "value": 25,
          "max": 25
        }
      },
      "wwiivillager:medic_trades": {
        "minecraft:trade_table": {
          "table": "trading/medic_trades.json"
        }
      }
    },
    "components": {
      "minecraft:type_family": {
        "family": ["villager", "mob", "human"]
      },
      "minecraft:health": {
        "value": 25,
        "max": 25
      },
      "minecraft:armor": {
        "slots": [
          {
            "slot": 0,
            "item": "wwiivillager:medic_helmet"
          },
          {
            "slot": 1,
            "item": "wwiivillager:medic_coat"
          }
        ]
      },
      "minecraft:movement": {
        "value": 0.5
      },
      "minecraft:behavior.look_at_player": {
        "priority": 0,
        "range": 6.0
      },
      "minecraft:behavior.random_look_around": {
        "priority": 1
      },
      "minecraft:behavior.wander": {
        "priority": 2,
        "speed_multiplier": 0.6
      },
      "minecraft:nameable": {
        "allow_name_tag_renaming": true
      }
    },
    "events": {
      "wwiivillager:medic_spawn": {
        "add": {
          "component_groups": ["wwiivillager:medic_base", "wwiivillager:medic_trades"]
        }
      }
    }
  }
}
{
  "format_version": "1.20.0",
  "minecraft:entity": {
    "description": {
      "identifier": "wwiivillager:engineer_villager",
      "is_spawnable": true,
      "is_summonable": true,
      "is_experimental": false
    },
    "component_groups": {
      "wwiivillager:engineer_base": {
        "minecraft:type_family": {
          "family": ["villager", "mob", "human"]
        },
        "minecraft:health": {
          "value": 22,
          "max": 22
        }
      },
      "wwiivillager:engineer_trades": {
        "minecraft:trade_table": {
          "table": "trading/engineer_trades.json"
        }
      }
    },
    "components": {
      "minecraft:type_family": {
        "family": ["villager", "mob", "human"]
      },
      "minecraft:health": {
        "value": 22,
        "max": 22
      },
      "minecraft:armor": {
        "slots": [
          {
            "slot": 0,
            "item": "wwiivillager:engineer_hat"
          },
          {
            "slot": 1,
            "item": "wwiivillager:engineer_coat"
          }
        ]
      },
      "minecraft:movement": {
        "value": 0.5
      },
      "minecraft:behavior.look_at_player": {
        "priority": 0,
        "range": 6.0
      },
      "minecraft:nameable": {
        "allow_name_tag_renaming": true
      }
    },
    "events": {
      "wwiivillager:engineer_spawn": {
        "add": {
          "component_groups": ["wwiivillager:engineer_base", "wwiivillager:engineer_trades"]
        }
      }
    }
  }
}
{
  "tiers": [
    {
      "tier": 0,
      "trades": [
        {
          "max_uses": 16,
          "buy": {
            "item": "minecraft:emerald",
            "quantity": 5
          },
          "sell": {
            "item": "wwiivillager:rifle",
            "quantity": 1
          }
        },
        {
          "max_uses": 12,
          "buy": {
            "item": "minecraft:emerald",
            "quantity": 3
          },
          "sell": {
            "item": "wwiivillager:ammunition",
            "quantity": 32
          }
        },
        {
          "max_uses": 8,
          "buy": {
            "item": "minecraft:emerald",
            "quantity": 4
          },
          "sell": {
            "item": "wwiivillager:grenade",
            "quantity": 2
          }
        }
      ]
    },
    {
      "tier": 1,
      "trades": [
        {
          "max_uses": 12,
          "buy": {
            "item": "minecraft:emerald",
            "quantity": 7
          },
          "sell": {
            "item": "wwiivillager:rifle_elite",
            "quantity": 1
          }
        },
        {
          "max_uses": 10,
          "buy": {
            "item": "minecraft:emerald",
            "quantity": 6
          },
          "sell": {
            "item": "wwiivillager:combat_boots",
            "quantity": 1
          }
        }
      ]
    }
  ]
}{
  "tiers": [
    {
      "tier": 0,
      "trades": [
        {
          "max_uses": 20,
          "buy": {
            "item": "minecraft:emerald",
            "quantity": 3
          },
          "sell": {
            "item": "wwiivillager:medkit",
            "quantity": 1
          }
        },
        {
          "max_uses": 16,
          "buy": {
            "item": "minecraft:emerald",
            "quantity": 2
          },
          "sell": {
            "item": "wwiivillager:bandage",
            "quantity": 4
          }
        },
        {
          "max_uses": 12,
          "buy": {
            "item": "minecraft:emerald",
            "quantity": 4
          },
          "sell": {
            "item": "minecraft:potion",
            "quantity": 1
          }
        }
      ]
    },
    {
      "tier": 1,
      "trades": [
        {
          "max_uses": 8,
          "buy": {
            "item": "minecraft:emerald",
            "quantity": 5
          },
          "sell": {
            "item": "wwiivillager:advanced_medkit",
            "quantity": 1
          }
        }
      ]
    }
  ]
}
{
  "tiers": [
    {
      "tier": 0,
      "trades": [
        {
          "max_uses": 16,
          "buy": {
            "item": "minecraft:emerald",
            "quantity": 4
          },
          "sell": {
            "item": "wwiivillager:tool_kit",
            "quantity": 1
          }
        },
        {
          "max_uses": 12,
          "buy": {
            "item": "minecraft:emerald",
            "quantity": 3
          },
          "sell": {
            "item": "wwiivillager:iron_parts",
            "quantity": 8
          }
        },
        {
          "max_uses": 10,
          "buy": {
            "item": "minecraft:emerald",
            "quantity": 6
          },
          "sell": {
            "item": "wwiivillager:canteen",
            "quantity": 1
          }
        }
      ]
    },
    {
      "tier": 1,
      "trades": [
        {
          "max_uses": 8,
          "buy": {
            "item": "minecraft:emerald",
            "quantity": 8
          },
          "sell": {
            "item": "wwiivillager:advanced_tool_kit",
            "quantity": 1
          }
        }
      ]
    }
  ]
}
{
  "format_version": "1.20.0",
  "minecraft:item": {
    "description": {
      "identifier": "wwiivillager:rifle",
      "category": "equipment"
    },
    "components": {
      "minecraft:icon": {
        "texture": "wwiivillager:rifle"
      },
      "minecraft:display_name": {
        "value": "Rifle"
      },
      "minecraft:durability": {
        "max_durability": 250
      },
      "minecraft:damage": {
        "range": [8, 12]
      },
      "minecraft:enchantable": {
        "value": 50
      },
      "minecraft:repairable": {
        "repair_items": ["minecraft:iron_ingot"]
      }
    }
  }
}
{
  "format_version": "1.20.0",
  "minecraft:item": {
    "description": {
      "identifier": "wwiivillager:medkit",
      "category": "consumable"
    },
    "components": {
      "minecraft:icon": {
        "texture": "wwiivillager:medkit"
      },
      "minecraft:display_name": {
        "value": "Medkit"
      },
      "minecraft:food": {
        "nutrition": 4,
        "saturation_modifier": 0.3,
        "effects": [
          {
            "name": "regeneration",
            "chance": 1.0,
            "duration": 100,
            "amplifier": 1
          }
        ]
      },
      "minecraft:use_animation": "eat",
      "minecraft:cooldown": {
        "category": "ender_pearl",
        "cooldown_type": "set",
        "cooldown_tick": 0
      }
    }
  }
}
{
  "format_version": "1.20.0",
  "minecraft:item": {
    "description": {
      "identifier": "wwiivillager:ammunition",
      "category": "equipment"
    },
    "components": {
      "minecraft:icon": {
        "texture": "wwiivillager:ammunition"
      },
      "minecraft:display_name": {
        "value": "Ammunition"
      },
      "minecraft:stackable": {
        "max_stack_size": 64
      }
    }
  }
}
{
  "format_version": "1.20.0",
  "minecraft:item": {
    "description": {
      "identifier": "wwiivillager:canteen",
      "category": "consumable"
    },
    "components": {
      "minecraft:icon": {
        "texture": "wwiivillager:canteen"
      },
      "minecraft:display_name": {
        "value": "Canteen"
      },
      "minecraft:food": {
        "nutrition": 2,
        "saturation_modifier": 0.4
      },
      "minecraft:use_animation": "drink",
      "minecraft:stackable": {
        "max_stack_size": 16
      }
    }
  }
}
{
  "format_version": "1.20.0",
  "minecraft:item": {
    "description": {
      "identifier": "wwiivillager:rations",
      "category": "consumable"
    },
    "components": {
      "minecraft:icon": {
        "texture": "wwiivillager:rations"
      },
      "minecraft:display_name": {
        "value": "Rations"
      },
      "minecraft:food": {
        "nutrition": 6,
        "saturation_modifier": 0.6,
        "effects": [
          {
            "name": "saturation",
            "chance": 0.8,
            "duration": 30,
            "amplifier": 0
          }
        ]
      },
      "minecraft:use_animation": "eat",
      "minecraft:stackable": {
        "max_stack_size": 64
      }
    }
  }
}
{
  "format_version": 2,
  "header": {
    "name": "WWII Villager - Resource Pack",
    "description": "Resource pack for WWII villager addon",
    "uuid": "550e8400-e29b-41d4-a716-446655440006",
    "version": [1, 0, 0],
    "min_engine_version": [1, 20, 0]
  },
  "modules": [
    {
      "description": "Resource Pack Module",
      "type": "resources",
      "uuid": "550e8400-e29b-41d4-a716-446655440007",
      "version": [1, 0, 0]
    }
  ]
}
{
  "resource_pack_name": "WWII Villager",
  "texture_name": "atlas.items",
  "texture_data": {
    "wwiivillager:rifle": {
      "textures": "textures/items/rifle"
    },
    "wwiivillager:rifle_elite": {
      "textures": "textures/items/rifle_elite"
    },
    "wwiivillager:ammunition": {
      "textures": "textures/items/ammunition"
    },
    "wwiivillager:grenade": {
      "textures": "textures/items/grenade"
    },
    "wwiivillager:medkit": {
      "textures": "textures/items/medkit"
    },
    "wwiivillager:bandage": {
      "textures": "textures/items/bandage"
    },
    "wwiivillager:advanced_medkit": {
      "textures": "textures/items/advanced_medkit"
    },
    "wwiivillager:tool_kit": {
      "textures": "textures/items/tool_kit"
    },
    "wwiivillager:advanced_tool_kit": {
      "textures": "textures/items/advanced_tool_kit"
    },
    "wwiivillager:iron_parts": {
      "textures": "textures/items/iron_parts"
    },
    "wwiivillager:canteen": {
      "textures": "textures/items/canteen"
    },
    "wwiivillager:rations": {
      "textures": "textures/items/rations"
    },
    "wwiivillager:combat_boots": {
      "textures": "textures/items/combat_boots"
    },
    "wwiivillager:military_helmet": {
      "textures": "textures/items/military_helmet"
    },
    "wwiivillager:military_chest": {
      "textures": "textures/items/military_chest"
    },
    "wwiivillager:military_legs": {
      "textures": "textures/items/military_legs"
    },
    "wwiivillager:medic_helmet": {
      "textures": "textures/items/medic_helmet"
    },
    "wwiivillager:medic_coat": {
      "textures": "textures/items/medic_coat"
    },
    "wwiivillager:engineer_hat": {
      "textures": "textures/items/engineer_hat"
    },
    "wwiivillager:engineer_coat": {
      "textures": "textures/items/engineer_coat"
    }
  }
}
{
  "resource_pack_name": "WWII Villager",
  "texture_data": {
    "soldier_villager": {
      "textures": [
        "textures/entity/villager/soldier/soldier"
      ]
    },
    "medic_villager": {
      "textures": [
        "textures/entity/villager/medic/medic"
      ]
    },
    "engineer_villager": {
      "textures": [
        "textures/entity/villager/engineer/engineer"
      ]
    }
  }
}
{
  "format_version": "1.12.0",
  "minecraft:geometry": [
    {
      "description": {
        "identifier": "geometry.soldier_villager",
        "texture_width": 64,
        "texture_height": 64,
        "visible_bounds_width": 1,
        "visible_bounds_height": 1.5,
        "visible_bounds_offset": [0, 0.5, 0]
      },
      "bones": [
        {
          "name": "root",
          "pivot": [0, 0, 0],
          "cubes": [
            {
              "origin": [-4, 0, -3],
              "size": [8, 8, 6],
              "uv": [0, 0]
            }
          ]
        },
        {
          "name": "body",
          "parent": "root",
          "pivot": [0, 8, 0],
          "cubes": [
            {
              "origin": [-4, 8, -2],
              "size": [8, 12, 4],
              "uv": [0, 16]
            }
          ]
        },
        {
          "name": "left_arm",
          "parent": "body",
          "pivot": [-4, 20, 0],
          "cubes": [
            {
              "origin": [-8, 8, -2],
              "size": [4, 12, 4],
              "uv": [32, 16]
            }
          ]
        },
        {
          "name": "right_arm",
          "parent": "body",
          "pivot": [4, 20, 0],
          "cubes": [
            {
              "origin": [4, 8, -2],
              "size": [4, 12, 4],
              "uv": [48, 16]
            }
          ]
        },
        {
          "name": "left_leg",
          "parent": "root",
          "pivot": [-2, 8, 0],
          "cubes": [
            {
              "origin": [-4, 0, -2],
              "size": [4, 8, 4],
              "uv": [16, 32]
            }
          ]
        },
        {
          "name": "right_leg",
          "parent": "root",
          "pivot": [2, 8, 0],
          "cubes": [
            {
              "origin": [0, 0, -2],
              "size": [4, 8, 4],
              "uv": [0, 32]
            }
          ]
        }
      ]
    }
  ]
}
item.wwiivillager:rifle.name=Rifle
item.wwiivillager:rifle_elite.name=Elite Rifle
item.wwiivillager:ammunition.name=Ammunition
item.wwiivillager:grenade.name=Grenade
item.wwiivillager:medkit.name=Medkit
item.wwiivillager:bandage.name=Bandage
item.wwiivillager:advanced_medkit.name=Advanced Medkit
item.wwiivillager:tool_kit.name=Tool Kit
item.wwiivillager:advanced_tool_kit.name=Advanced Tool Kit
item.wwiivillager:iron_parts.name=Iron Parts
item.wwiivillager:canteen.name=Canteen
item.wwiivillager:rations.name=Rations
item.wwiivillager:combat_boots.name=Combat Boots
item.wwiivillager:military_helmet.name=Military Helmet
item.wwiivillager:military_chest.name=Military Chest Plate
item.wwiivillager:military_legs.name=Military Pants

entity.wwiivillager:soldier_villager.name=Soldier
entity.wwiivillager:medic_villager.name=Medic
entity.wwiivillager:engineer_villager.name=Engineer
item.wwiivillager:rifle.name=소총
item.wwiivillager:rifle_elite.name=엘리트 소총
item.wwiivillager:ammunition.name=탄약
item.wwiivillager:grenade.name=수류탄
item.wwiivillager:medkit.name=응급처치 키트
item.wwiivillager:bandage.name=붕대
item.wwiivillager:advanced_medkit.name=고급 응급처치 키트
item.wwiivillager:tool_kit.name=도구 키트
item.wwiivillager:advanced_tool_kit.name=고급 도구 키트
item.wwiivillager:iron_parts.name=철 부품
item.wwiivillager:canteen.name=물통
item.wwiivillager:rations.name=행군식량
item.wwiivillager:combat_boots.name=전투 부츠
item.wwiivillager:military_helmet.name=군사 헬멧
item.wwiivillager:military_chest.name=군사 흉갑
item.wwiivillager:military_legs.name=군사 바지

entity.wwiivillager:soldier_villager.name=군인
entity.wwiivillager:medic_villager.name=의무병
entity.wwiivillager:engineer_villager.name=공병
{
  "format_version": "1.0",
  "icon": "pack_icon.png"
}
WWII_Villager_Addon/
├── manifest.json
├── behavior_packs/
│   └── wwii_villager_bp/
│       ├── manifest.json
│       ├── entities/
│       │   ├── soldier_villager.json
│       │   ├── medic_villager.json
│       │   └── engineer_villager.json
│       ├── items/
│       │   ├── rifle.json
│       │   ├── medkit.json
│       │   ├── ammunition.json
│       │   ├── canteen.json
│       │   └── rations.json
│       └── trading/
│           ├── soldier_trades.json
│           ├── medic_trades.json
│           └── engineer_trades.json
├── resource_packs/
│   └── wwii_villager_rp/
│       ├── manifest.json
│       ├── textures/
│       │   ├── item_texture.json
│       │   └── entity_texture.json
│       ├── models/
│       │   └── entity/
│       │       └── soldier_villager.json
│       ├── lang/
│       │   ├── en_US.lang
│       │   └── ko_KR.lang
│       └── pack_icon.json

