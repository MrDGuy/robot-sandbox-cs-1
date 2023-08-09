# Robot Sandbox

## Create your own Robot world @unplugged

Here there are no boundaries only creativity!  You have all the available robot code to create your own custom creations.  Have fun!


## Robot code

Use the commands and conditions in the robot category.
```python
    robot.begin_screen()
    robot.move_forward()
    robot.turn_right()
    robot.turn_left()
    robot.place_coin()
    robot.collect_coin()
    robot.get_direction()
    robot.change_robot(img(""" """), img(""" """), img(""" """), img(""" """))
    robot.detect_coin()
    robot.can_move("")
```

## Custom Tilemaps code

You can also use tilemaps commands:

```python
    tile_map1 = tiles.create_map(tilemap("""level1"""))
    tile_map2 = tiles.create_map(tilemap("""level2"""))
    tiles.load_map(tile_map1)
    tiles.connect_map_by_id(tilemap1, tilemap2, ConnectionKind.door1)

    def on_overlap_tile(sprite, location):
        tiles.load_map(tile_map2)
        robot.begin_screen()
    scene.on_overlap_tile(SpriteKind.player, img(""" """), on_overlap_tile)
```

## Functions, Loops and If Statements

Use different control structures to make your code more abstract.

```python
  def do_something():
    pass

  for i in range(4):
    pass

  if robot.can_move("forward"):
    pass

  if robot.can_move("forward"):
    pass
  else:
    pass


```assetjson
{
  "README.md": " ",
  "assets.json": "",
  "main.blocks": "<xml xmlns=\"https://developers.google.com/blockly/xml\"><block type=\"pxt-on-start\" x=\"0\" y=\"0\"></block><block type=\"forever\" x=\"110\" y=\"190\"><statement name=\"HANDLER\"><block type=\"controls_if\"><value name=\"IF0\"><shadow type=\"logic_boolean\"><field name=\"BOOL\">TRUE</field></shadow><block type=\"robot_goalReached\"><field name=\"goalTile\">sprites.background.autumn</field></block></value><statement name=\"DO0\"><block type=\"game_setgameovereffect\"><field name=\"effect\">effects.confetti</field><value name=\"win\"><shadow type=\"toggleWinLose\"><field name=\"win\">true</field></shadow></value><next><block type=\"game_setgameoverplayable\"><value name=\"sound\"><shadow type=\"music_melody_playable\"><field name=\"melody\">music.powerUp</field></shadow></value><value name=\"looping\"><shadow type=\"toggleOnOff\"><field name=\"on\">true</field></shadow></value><value name=\"win\"><shadow type=\"toggleWinLose\"><field name=\"win\">true</field></shadow></value><next><block type=\"game_setgameovermessage\"><value name=\"message\"><shadow type=\"text\"><field name=\"TEXT\">Goal Reached!</field></shadow></value><value name=\"win\"><shadow type=\"toggleWinLose\"><field name=\"win\">true</field></shadow></value></block></next></block></next></block></statement></block></statement></block></xml>",
  "main.py": "",
  "main.ts": "\n",
  "pxt.json": "{\n    \"name\": \"Non Git Hub Robot Tile and Tilemap Assets - Copy\",\n    \"description\": \"\",\n    \"dependencies\": {\n        \"device\": \"*\",\n        \"tilemaps\": \"github:microsoft/pxt-tilemaps#v1.12.0\",\n        \"Sprite Grid\": \"github:microsoft/arcade-grid#v1.3.0\",\n        \"Robot Extension\": \"github:MrDGuy/robot-extension#8a70c12520c14e7caf22006addbea36f5267078f\"\n    },\n    \"files\": [\n        \"main.blocks\",\n        \"main.ts\",\n        \"README.md\",\n        \"assets.json\",\n        \"tilemap.g.jres\",\n        \"tilemap.g.ts\",\n        \"main.py\"\n    ],\n    \"targetVersions\": {\n        \"branch\": \"v1.13.31\",\n        \"tag\": \"v1.13.31\",\n        \"commits\": \"https://github.com/microsoft/pxt-arcade/commits/ef3aad740700f5159eebccf721fa35d32683fcaa\",\n        \"target\": \"1.13.31\",\n        \"pxt\": \"9.1.6\"\n    },\n    \"preferredEditor\": \"pyprj\"\n}\n",
  "tilemap.g.jres": "{\n    \"tile1\": {\n        \"data\": \"hwQQABAAAAD//////////09ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPT//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"startTile\"\n    },\n    \"tile2\": {\n        \"data\": \"hwQQABAAAAD//////////4+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPj//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"goalTile\"\n    },\n    \"tile3\": {\n        \"data\": \"hwQQABAAAAD//////////x8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfH//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"floorTile\"\n    },\n    \"transparency16\": {\n        \"data\": \"hwQQABAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true\n    },\n    \"tile4\": {\n        \"data\": \"hwQQABAAAAD//////////393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/f//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"coinTile\"\n    },\n    \"*\": {\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"dataEncoding\": \"base64\",\n        \"namespace\": \"myTiles\"\n    }\n}",
  "tilemap.g.ts": "// Auto-generated code. Do not edit.\nnamespace myTiles {\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile1 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile2 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile3 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const transparency16 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile4 = image.ofBuffer(hex``);\n\n    helpers._registerFactory(\"tile\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"startTile\":\n            case \"tile1\":return tile1;\n            case \"goalTile\":\n            case \"tile2\":return tile2;\n            case \"floorTile\":\n            case \"tile3\":return tile3;\n            case \"transparency16\":return transparency16;\n            case \"coinTile\":\n            case \"tile4\":return tile4;\n        }\n        return null;\n    })\n\n}\n// Auto-generated code. Do not edit.\n"
}
```
```template
tiles.loadMap(tiles.createMap(tilemap`level1`))
robot.beginScreen()
game.onUpdate(function () {
    if (robot.goalReached()) {
        music.play(music.melodyPlayable(music.powerUp), music.PlaybackMode.UntilDone)
        game.splash("You reached the goal!")
        game.reset()
    }
})
```

