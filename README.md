---- Minecraft Crash Report ----
// There are four lights!

Time: 25.04.20 20:30
Description: Ticking block entity

java.lang.ArithmeticException: Division by zero
	at mekanism.api.math.FloatingLong.divideEquals(FloatingLong.java:329) ~[?:?] {re:classloading}
	at mekanism.api.math.FloatingLong.divide(FloatingLong.java:471) ~[?:?] {re:classloading}
	at mekanism.generators.common.tile.turbine.TileEntityTurbineCasing.onUpdateServer(TileEntityTurbineCasing.java:66) ~[?:?] {re:classloading}
	at mekanism.common.tile.base.TileEntityMekanism.func_73660_a(TileEntityMekanism.java:470) ~[?:?] {re:classloading}
	at net.minecraft.world.World.func_217391_K(World.java:473) ~[?:?] {re:classloading,pl:accesstransformer:B}
	at net.minecraft.world.server.ServerWorld.func_72835_b(ServerWorld.java:368) ~[?:?] {re:classloading}
	at net.minecraft.server.MinecraftServer.func_71190_q(MinecraftServer.java:849) ~[?:?] {re:classloading,pl:accesstransformer:B}
	at net.minecraft.server.MinecraftServer.func_71217_p(MinecraftServer.java:784) ~[?:?] {re:classloading,pl:accesstransformer:B}
	at net.minecraft.server.integrated.IntegratedServer.func_71217_p(IntegratedServer.java:114) ~[?:?] {re:classloading,pl:runtimedistcleaner:A}
	at net.minecraft.server.MinecraftServer.run(MinecraftServer.java:637) [?:?] {re:classloading,pl:accesstransformer:B}
	at java.lang.Thread.run(Unknown Source) [?:1.8.0_241] {}


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- Head --
Thread: Server thread
Stacktrace:
	at mekanism.api.math.FloatingLong.divideEquals(FloatingLong.java:329)
	at mekanism.api.math.FloatingLong.divide(FloatingLong.java:471)
	at mekanism.generators.common.tile.turbine.TileEntityTurbineCasing.onUpdateServer(TileEntityTurbineCasing.java:66)
	at mekanism.common.tile.base.TileEntityMekanism.func_73660_a(TileEntityMekanism.java:470)

-- Block entity being ticked --
Details:
	Name: mekanismgenerators:turbine_casing // mekanism.generators.common.tile.turbine.TileEntityTurbineCasing
	Block: Block{mekanismgenerators:turbine_casing}
	Block location: World: (-773,84,-1091), Chunk: (at 11,5,13 in -49,-69; contains blocks -784,0,-1104 to -769,255,-1089), Region: (-2,-3; contains chunks -64,-96 to -33,-65, blocks -1024,0,-1536 to -513,255,-1025)
	Block: Block{mekanismgenerators:turbine_casing}
	Block location: World: (-773,84,-1091), Chunk: (at 11,5,13 in -49,-69; contains blocks -784,0,-1104 to -769,255,-1089), Region: (-2,-3; contains chunks -64,-96 to -33,-65, blocks -1024,0,-1536 to -513,255,-1025)
Stacktrace:
	at net.minecraft.world.World.func_217391_K(World.java:473)
	at net.minecraft.world.server.ServerWorld.func_72835_b(ServerWorld.java:368)

-- Affected level --
Details:
	All players: 1 total; [ServerPlayerEntity['Sam2k'/9515, l='Новый мир', x=-771.70, y=86.82, z=-1087.30]]
	Chunk stats: ServerChunkCache: 4234
	Level dimension: DimensionType{minecraft:overworld}
	Level name: Новый мир
	Level seed: -5706255176791544044
	Level generator: ID 00 - default, ver 1. Features enabled: true
	Level generator options: {}
	Level spawn location: World: (65,63,24), Chunk: (at 1,3,8 in 4,1; contains blocks 64,0,16 to 79,255,31), Region: (0,0; contains chunks 0,0 to 31,31, blocks 0,0,0 to 511,255,511)
	Level time: 35654 game time, 35654 day time
	Known server brands: forge
	Level was modded: true
	Level storage version: 0x04ABD - Anvil
	Level weather: Rain time: 143395 (now: false), thunder time: 37461 (now: false)
	Level game mode: Game mode: creative (ID 1). Hardcore: false. Cheats: false
Stacktrace:
	at net.minecraft.server.MinecraftServer.func_71190_q(MinecraftServer.java:849)
	at net.minecraft.server.MinecraftServer.func_71217_p(MinecraftServer.java:784)
	at net.minecraft.server.integrated.IntegratedServer.func_71217_p(IntegratedServer.java:114)
	at net.minecraft.server.MinecraftServer.run(MinecraftServer.java:637)
	at java.lang.Thread.run(Unknown Source)

-- System Details --
Details:
	Minecraft Version: 1.15.2
	Minecraft Version ID: 1.15.2
	Operating System: Windows 10 (amd64) version 10.0
	Java Version: 1.8.0_241, Oracle Corporation
	Java VM Version: Java HotSpot(TM) 64-Bit Server VM (mixed mode), Oracle Corporation
	Memory: 682719448 bytes (651 MB) / 2396160000 bytes (2285 MB) up to 3207856128 bytes (3059 MB)
	CPUs: 8
	JVM Flags: 5 total; -Xmn128M -Xmx3072M -XX:HeapDumpPath=MojangTricksIntelDriversForPerformance_javaw.exe_minecraft.exe.heapdump -Xss1M -XX:+UseConcMarkSweepGC
	ModLauncher: 5.0.0-milestone.4+67+b1a340b
	ModLauncher launch target: fmlclient
	ModLauncher naming: srg
	ModLauncher services: 
		/eventbus-2.0.0-milestone.1-service.jar eventbus PLUGINSERVICE 
		/forge-1.15.2-31.1.44.jar object_holder_definalize PLUGINSERVICE 
		/forge-1.15.2-31.1.44.jar runtime_enum_extender PLUGINSERVICE 
		/accesstransformers-2.0.4-shadowed.jar accesstransformer PLUGINSERVICE 
		/forge-1.15.2-31.1.44.jar capability_inject_definalize PLUGINSERVICE 
		/forge-1.15.2-31.1.44.jar runtimedistcleaner PLUGINSERVICE 
		/forge-1.15.2-31.1.44.jar fml TRANSFORMATIONSERVICE 
	FML: 31.1
	Forge: net.minecraftforge:31.1.44
	FML Language Providers: 
		javafml@31.1
		minecraft@1
	Mod List: 
		followingvillagers-1.15.2-1.4.0.jar Following Villagers {followingvillagers@1.15.2-1.4.0 DONE}
		ClientTweaks_1.15.2-4.1.1.jar Client Tweaks {clienttweaks@4.1.1 DONE}
		Cucumber-1.15.2-3.0.3.jar Cucumber Library {cucumber@3.0.3 DONE}
		mining-helmet-1.15.2-1.0.8.jar Mining Helmet {mining_helmet@1.0.8 DONE}
		jei-1.15.2-6.0.0.3.jar Just Enough Items {jei@6.0.0.3 DONE}
		crawl-1.15.2-1.0.jar Press C To Crawl {crawl@1.15.2-1.0 DONE}
		Mekanism-1.15.2-9.10.1.414.jar Mekanism {mekanism@9.10.1 DONE}
		mcw-windows-1.0.1-mc1.15.2_1.15.1.jar Macaw's Windows {mcwwindows@1.0.1 DONE}
		caelus-FORGE-1.15.2-2.0-beta2.jar Caelus API {caelus@FORGE-1.15.2-2.0-beta2 DONE}
		BetterStorageToo-1.15.2-5.0.1.0.jar BetterStorageToo {betterstorage@1.15.2-5.0.1.0 DONE}
		SneakyMagic-v2.0-1.15.2.jar Sneaky Magic {sneakymagic@2.0 DONE}
		colytra-FORGE-1.15.2-3.0.jar Colytra {colytra@FORGE-1.15.2-3.0 DONE}
		rsgauges-1.15.2-1.2.2.jar Gauges and Switches {rsgauges@1.2.2 DONE}
		IronJetpacks-1.15.2-3.0.1.jar Iron Jetpacks {ironjetpacks@3.0.1 DONE}
		ForgeEndertech-1.15.2-6.0.1.0-build.0011.jar Forge Endertech {forgeendertech@6.0.1.0 DONE}
		AdFinders-1.15.2-4.0.3.0-build.0014.jar Advanced Finders {adfinders@4.0.3.0 DONE}
		journeymap-1.15.2-5.7.0beta1.jar Journeymap {journeymap@1.15.2-5.7.0beta1 DONE}
		decorative_blocks-6d.jar Decorative Blocks {decorative_blocks@1.6 DONE}
		AdHooks-1.15.2-5.0.0.0-build.0004.jar Advanced Hook Launchers {adhooks@5.0.0.0 DONE}
		Bookshelf-1.15.2-5.3.11.jar Bookshelf {bookshelf@5.3.11 DONE}
		BotanyPots-1.15.2-2.0.9.jar BotanyPots {botanypots@2.0.9 DONE}
		buildinggadgets-3.3.4.jar Building Gadgets {buildinggadgets@3.3.4 DONE}
		DarkUtilities-1.15.2-3.0.3.jar Dark Utilities {darkutils@3.0.3 DONE}
		ProgressiveBosses-2.1.5-mc1.15.2.jar Progressive Bosses {progressivebosses@2.1.5-mc1.15.2 DONE}
		mapperbase-1.15.2-1.0.0.1.jar Mapper Base {mapperbase@1.15.2-1.0.0.1 DONE}
		MekanismGenerators-1.15.2-9.10.1.414.jar Mekanism: Generators {mekanismgenerators@9.10.1 DONE}
		walljump-forge-1.15.2-1.3.5.jar Wall-Jump! {walljump@1.15.2-1.3.5 DONE}
		forge-1.15.2-31.1.44-universal.jar Forge {forge@31.1.44 DONE}
		refinedstorage-1.8.1.jar Refined Storage {refinedstorage@1.8.1 DONE}
		ironchest-1.15.2-10.0.3.jar Iron Chests {ironchest@1.15.2-10.0.1 DONE}
		forge-1.15.2-31.1.44-client.jar Minecraft {minecraft@1.15.2 DONE}
		mcw-bridges-1.0.4fix-mc1.15.2.jar Macaw's Bridges {mcwbridges@1.0.4 DONE}
		lightestlampsmod-3.4.0.jar Lightest Lamps {lightestlamp@3.4.0 DONE}
		industrial-foregoing-1.15.2-2.2.2-28d4a81.jar Industrial Foregoing {industrialforegoing@2.2.2 DONE}
		EnchantmentDescriptions-1.15.2-2.0.8.jar EnchantmentDescriptions {enchdesc@2.0.8 DONE}
		embellishcraft-1.15.2-2.1.0.1.jar EmbellishCraft {embellishcraft@1.15.2-2.1.0.1 DONE}
		MouseTweaks-2.13-mc1.15.1.jar Mouse Tweaks {mousetweaks@2.13 DONE}
		GreaterEye-1.15.2-1.0.4.jar GreaterEye {greater_eye@1.0.4 DONE}
		titanium-1.15.2-2.3.7.jar Titanium {titanium@2.3.7 DONE}
		MekanismAdditions-1.15.2-9.10.1.414.jar Mekanism: Additions {mekanismadditions@9.10.1 DONE}
		valkyrielib-1.15.2-3.0.2.1.jar ValkyrieLib {valkyrielib@1.15.2-3.0.2.1 DONE}
		simplechunkloaders-1.15.2-1.0.2.0.jar Simple Chunk Loaders {simplechunkloaders@NONE DONE}
		ShoulderSurfing-1.15.2-1.22.4.jar Shoulder Surfing {shouldersurfing@1.15.2-1.22.4 DONE}
		movingelevators-1.2.3-mc1.15.jar Moving Elevators {movingelevators@1.2.3 DONE}
		SoulShardsRespawn-forge-1.15.2-1.2.0-15.jar Soul Shards Respawn {soulshards@version DONE}
		simplylight-1.15.2-0.9.0.jar Simply Light {simplylight@1.15.2-0.9.0 DONE}
		simplybackpacks-1.15.2-1.4.5.jar Simply Backpacks {simplybackpacks@1.15.2-1.4.5 DONE}
		MaterialMaster-v1.1.3-1.15.2.jar Material Master {materialmaster@1.1.3 DONE}
		pamhc2foodcore-1.15.2-1.0.3.jar Pam's HarvestCraft 2 Food Core {pamhc2foodcore@version DONE}
		StorageDrawers-1.15.2-7.0.2.jar Storage Drawers {storagedrawers@1.15.2-7.0.1 DONE}
		OreExcavation-1.7.151.jar Ore Excavation {oreexcavation@NONE DONE}
		backpacked-1.4.1-mc1.15.2.jar Backpacked {backpacked@1.4.1 DONE}
		elevatorid-1.15.2-1.7.0.jar Elevator Mod {elevatorid@1.15.2-1.7.0 DONE}
		Gobber2-1.15.2-2.2.80.jar Gobber 2 {gobber2@2.2.80 DONE}
		tombstone-4.3.4-1.15.2.jar Corail Tombstone {tombstone@4.3.4 DONE}
		obfuscate-0.4.1-1.15.2.jar Obfuscate {obfuscate@0.4.1 DONE}
		vehicle-0.43.5-mc1.15.2.jar MrCrayfish's Vehicle Mod {vehicle@0.43.5 DONE}
		MekanismTools-1.15.2-9.10.1.414.jar Mekanism: Tools {mekanismtools@9.10.1 DONE}
		mcw-roofs-1.0.2-mc1.15.2_1.15.1.jar Macaw's Roofs {mcwroofs@1.0.2 DONE}
		cfm-7.0.0-pre16-mc1.15.1.jar MrCrayfish's Furniture Mod {cfm@7.0.0-pre16 DONE}
		AppleSkin-mc1.15.2-forge-1.0.13.jar AppleSkin {appleskin@1.0.13 DONE}
		mcw-furniture-1.0.1-mc1.15.1+1.15.2.jar Macaw's Furnitures {mcwfurnitures@1.0.1 DONE}
		refinedstorageaddons-0.6.1.jar Refined Storage Addons {refinedstorageaddons@0.6.1 DONE}
		FastLeafDecay-v20.jar FastLeafDecay {fastleafdecay@v20 DONE}
		Disenchanting_(forge)_1.15.2-1.2.0.jar Disenchanting {disenchanting@1.2.0 DONE}
		SoundFilters-0.13_for_1.15.2.jar Sound Filters {soundfilters@0.13_for_1.15.2 DONE}
	Player Count: 1 / 8; [ServerPlayerEntity['Sam2k'/9515, l='Новый мир', x=-771.70, y=86.82, z=-1087.30]]
	Data Packs: vanilla, mod:adfinders (incompatible), mod:adhooks (incompatible), mod:appleskin (incompatible), mod:backpacked (incompatible), mod:betterstorage (incompatible), mod:bookshelf (incompatible), mod:botanypots (incompatible), mod:buildinggadgets (incompatible), mod:caelus (incompatible), mod:cfm (incompatible), mod:clienttweaks (incompatible), mod:colytra (incompatible), mod:crawl (incompatible), mod:cucumber, mod:darkutils (incompatible), mod:decorative_blocks, mod:disenchanting (incompatible), mod:elevatorid, mod:embellishcraft (incompatible), mod:enchdesc (incompatible), mod:fastleafdecay, mod:followingvillagers (incompatible), mod:forge (incompatible), mod:forgeendertech (incompatible), mod:gobber2 (incompatible), mod:greater_eye (incompatible), mod:industrialforegoing (incompatible), mod:ironchest, mod:ironjetpacks, mod:jei (incompatible), mod:journeymap (incompatible), mod:lightestlamp, mod:mapperbase, mod:materialmaster, mod:mcwbridges, mod:mcwfurnitures, mod:mcwroofs, mod:mcwwindows, mod:mekanism, mod:mekanismadditions, mod:mekanismgenerators, mod:mekanismtools, mod:mining_helmet (incompatible), mod:mousetweaks (incompatible), mod:movingelevators, mod:obfuscate (incompatible), mod:oreexcavation (incompatible), mod:pamhc2foodcore (incompatible), mod:progressivebosses, mod:refinedstorage (incompatible), mod:refinedstorageaddons (incompatible), mod:rsgauges, mod:shouldersurfing (incompatible), mod:simplechunkloaders (incompatible), mod:simplybackpacks (incompatible), mod:simplylight (incompatible), mod:sneakymagic, mod:soulshards (incompatible), mod:soundfilters (incompatible), mod:storagedrawers (incompatible), mod:titanium (incompatible), mod:tombstone, mod:valkyrielib (incompatible), mod:vehicle (incompatible), mod:walljump
	Type: Integrated Server (map_client.txt)
	Is Modded: Definitely; Client brand changed to 'forge'
