How to install:
1. Place the ENTIRE "DeviTools" folder into your UE Projects Plugin Folder:

2. In your content/marvel folder create a new folder named "ImportedMaterials"

3. Enable Python: Make sure "Python Editor Script Plugin" is enabled in Edit -> Plugins.
4. Enable EditorUtilites: Make sure "Editor Scripting Utilites" is enabled in Edit -> Plugins. 


How to use: 
After importing your fbx ->
Place all your materials into /Content/Marvel/ImportedMaterials (you dont need to do this if you are only using the slotname function).

Run the Tool: Click the DeviTools Icon in your toolbar and wait for the widget to appear. 
Select your Skeletal Mesh and click the buttons you want to use. 


USAGE: 

Slot Name Updater: 
It updates the slot names of your skeletalmesh. 
This requires you to have fixed your material order in blender, if it is incorrect the plugin will only change the names it can detect. 
So like always, make sure to keep your characters OG materials at the start of the material list. 
This also means that it will change the material SLOTNAME of any custom/extra materials in your list if your material list is not a copy of the original one. 

Material Sorter: 
This function moves your materials from the ImportedMaterials folder into their respective correct folder path (for example: 1060/1060001/Materials/Lobby).
This function also looks for duplicates/dummy materials you might have used in blender to keep a slot open for a material. 
(for example: slot 1 and 6 both use 1060_1060001_hair_02. So you named your slot 6 material 1060_1060001_hair_022, this function will then assign 
the 1060_1060001_hair_02 to both those slots). 

Another thing this function does is rename a duplicate if they are supposed to be placed in two places. I've yet to see this in any other
character than White fox, but there might be I guess. ( So if 1060_hair is supposed to go in 1060001/Materials AND VFX/Character/1060 the script will look for 
duplicates/dummys and then rename them to match the original and then move them and of course assign them to the material slot). 


ALSO: The Material Sorter require you to name your duplicates/dummys the same as the original material name with one of the following suffixes: 
["1", "11", "111", "2", "22", "3", "33", "_1", "_2", "_011", "_0111", "_022", "_0222", "_033", "_0333"] 

[Example: 1060_1060001_Hair_02 - 1060_1060001_Hair_022 - 1060_1060001_Hair_0222 ]

Material Mover: 
This function just moves materials. It works the same way the Material Sorter does, but it ONLY moves materials, it doesnt look for duplicates 
or assign materials in the material slots. 

NOTE: 

I still haven't had the chance to test this tool on all characters, therefore issues can occur. If they do just let me know. 

Also this is fairly new, I've used it for a while but the code has been updated multiple times and obvi not tested in all enviroments, so issues tend to show when the script is used by other people. Anyway point is, if something isnt working out just let me know. 
