# Armorplus-DragonTeam-Log-Issue-Crash---Troubleshooting

---- Minecraft Crash Report ----

WARNING: coremods are present:
  ColytraLoadingPlugin (colytra-1.12.2-1.0.4.2.jar)
  ForgelinPlugin (Forgelin-1.6.0.jar)
  MMFMLCorePlugin (MultiMine-1.12.2.jar)
  BCModPlugin (backpacks+1.12.2+-+3.4.4.jar)
  LoadingPlugin (Quark-r1.4-123.jar)
  FCFMLCorePlugin (FinderCompass-1.12.1.jar)
  BetterFoliageLoader (BetterFoliage-MC1.12-2.1.10.jar)
Contact their authors BEFORE contacting forge

// You should try our sister game, Minceraft!

Time: 5/20/18 8:23 PM
Description: Ticking player

java.lang.IndexOutOfBoundsException: Index: 1, Size: 1
	at java.util.ArrayList.rangeCheck(ArrayList.java:653)
	at java.util.ArrayList.get(ArrayList.java:429)
	at net.thedragonteam.armorplus.armors.APArmorMaterial.lambda$addEffects$0(APArmorMaterial.java:363)
	at net.thedragonteam.armorplus.armors.APArmorMaterial$$Lambda$649/1915951550.accept(Unknown Source)
	at java.util.stream.Streams$RangeIntSpliterator.forEachRemaining(Streams.java:110)
	at java.util.stream.IntPipeline$Head.forEach(IntPipeline.java:557)
	at net.thedragonteam.armorplus.armors.APArmorMaterial.addEffects(APArmorMaterial.java:360)
	at net.thedragonteam.armorplus.armors.APArmorMaterial.addPieceEffects(APArmorMaterial.java:353)
	at net.thedragonteam.armorplus.armors.APArmorMaterial.addPieceEffects(APArmorMaterial.java:344)
	at net.thedragonteam.armorplus.armors.APArmorMaterial.addEffects(APArmorMaterial.java:332)
	at net.thedragonteam.armorplus.armors.APArmorMaterial$7.onArmorTick(APArmorMaterial.java:128)
	at net.thedragonteam.armorplus.armors.base.ItemArmorBase.onArmorTick(ItemArmorBase.java:127)
	at net.minecraft.entity.player.InventoryPlayer.func_70429_k(InventoryPlayer.java:371)
	at net.minecraft.entity.player.EntityPlayer.func_70636_d(EntityPlayer.java:511)
	at net.minecraft.entity.EntityLivingBase.func_70071_h_(EntityLivingBase.java:2170)
	at net.minecraft.entity.player.EntityPlayer.func_70071_h_(EntityPlayer.java:234)
	at net.minecraft.entity.player.EntityPlayerMP.func_71127_g(EntityPlayerMP.java:382)
	at net.minecraft.network.NetHandlerPlayServer.func_73660_a(NetHandlerPlayServer.java:173)
	at net.minecraftforge.fml.common.network.handshake.NetworkDispatcher$1.func_73660_a(NetworkDispatcher.java:209)
	at net.minecraft.network.NetworkManager.func_74428_b(NetworkManager.java:285)
	at net.minecraft.network.NetworkSystem.func_151269_c(NetworkSystem.java:180)
	at net.minecraft.server.MinecraftServer.func_71190_q(MinecraftServer.java:788)
	at net.minecraft.server.MinecraftServer.func_71217_p(MinecraftServer.java:666)
	at net.minecraft.server.integrated.IntegratedServer.func_71217_p(IntegratedServer.java:252)
	at net.minecraft.server.MinecraftServer.run(MinecraftServer.java:524)
	at java.lang.Thread.run(Thread.java:745)


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- Head --
Thread: Server thread
Stacktrace:
	at java.util.ArrayList.rangeCheck(ArrayList.java:653)
	at java.util.ArrayList.get(ArrayList.java:429)
	at net.thedragonteam.armorplus.armors.APArmorMaterial.lambda$addEffects$0(APArmorMaterial.java:363)
	at net.thedragonteam.armorplus.armors.APArmorMaterial$$Lambda$649/1915951550.accept(Unknown Source)
	at java.util.stream.Streams$RangeIntSpliterator.forEachRemaining(Streams.java:110)
	at java.util.stream.IntPipeline$Head.forEach(IntPipeline.java:557)
	at net.thedragonteam.armorplus.armors.APArmorMaterial.addEffects(APArmorMaterial.java:360)
	at net.thedragonteam.armorplus.armors.APArmorMaterial.addPieceEffects(APArmorMaterial.java:353)
	at net.thedragonteam.armorplus.armors.APArmorMaterial.addPieceEffects(APArmorMaterial.java:344)
	at net.thedragonteam.armorplus.armors.APArmorMaterial.addEffects(APArmorMaterial.java:332)
	at net.thedragonteam.armorplus.armors.APArmorMaterial$7.onArmorTick(APArmorMaterial.java:128)
	at net.thedragonteam.armorplus.armors.base.ItemArmorBase.onArmorTick(ItemArmorBase.java:127)
	at net.minecraft.entity.player.InventoryPlayer.func_70429_k(InventoryPlayer.java:371)
	at net.minecraft.entity.player.EntityPlayer.func_70636_d(EntityPlayer.java:511)
	at net.minecraft.entity.EntityLivingBase.func_70071_h_(EntityLivingBase.java:2170)
	at net.minecraft.entity.player.EntityPlayer.func_70071_h_(EntityPlayer.java:234)

-- Player being ticked --
Details:
	Entity Type: null (net.minecraft.entity.player.EntityPlayerMP)
	Entity ID: 134
	Entity Name: Iteries
	Entity's Exact location: 177.33, 32.00, -1280.27
	Entity's Block location: World: (177,32,-1281), Chunk: (at 1,2,15 in 11,-81; contains blocks 176,0,-1296 to 191,255,-1281), Region: (0,-3; contains chunks 0,-96 to 31,-65, blocks 0,0,-1536 to 511,255,-1025)
	Entity's Momentum: 0.00, -0.08, 0.00
	Entity's Passengers: []
	Entity's Vehicle: ~~ERROR~~ NullPointerException: null
Stacktrace:
	at net.minecraft.entity.player.EntityPlayerMP.func_71127_g(EntityPlayerMP.java:382)
	at net.minecraft.network.NetHandlerPlayServer.func_73660_a(NetHandlerPlayServer.java:173)
	at net.minecraftforge.fml.common.network.handshake.NetworkDispatcher$1.func_73660_a(NetworkDispatcher.java:209)
	at net.minecraft.network.NetworkManager.func_74428_b(NetworkManager.java:285)

-- Ticking connection --
Details:
	Connection: net.minecraft.network.NetworkManager@285adde5
Stacktrace:
	at net.minecraft.network.NetworkSystem.func_151269_c(NetworkSystem.java:180)
	at net.minecraft.server.MinecraftServer.func_71190_q(MinecraftServer.java:788)
	at net.minecraft.server.MinecraftServer.func_71217_p(MinecraftServer.java:666)
	at net.minecraft.server.integrated.IntegratedServer.func_71217_p(IntegratedServer.java:252)
	at net.minecraft.server.MinecraftServer.run(MinecraftServer.java:524)
	at java.lang.Thread.run(Thread.java:745)

-- System Details --
Details:
	Minecraft Version: 1.12.2
	Operating System: Windows 10 (amd64) version 10.0
	Java Version: 1.8.0_25, Oracle Corporation
	Java VM Version: Java HotSpot(TM) 64-Bit Server VM (mixed mode), Oracle Corporation
	Memory: 1197546488 bytes (1142 MB) / 4294967296 bytes (4096 MB) up to 4294967296 bytes (4096 MB)
	JVM Flags: 8 total; -XX:HeapDumpPath=MojangTricksIntelDriversForPerformance_javaw.exe_minecraft.exe.heapdump -Xmx4G -XX:+UnlockExperimentalVMOptions -XX:+UseG1GC -XX:G1NewSizePercent=20 -XX:G1ReservePercent=20 -XX:MaxGCPauseMillis=50 -XX:G1HeapRegionSize=16M
	IntCache: cache: 0, tcache: 0, allocated: 0, tallocated: 37
	FML: MCP 9.42 Powered by Forge 14.23.2.2654 Optifine OptiFine_1.12.2_HD_U_D1 35 mods loaded, 35 mods active
	States: 'U' = Unloaded 'L' = Loaded 'C' = Constructed 'H' = Pre-initialized 'I' = Initialized 'J' = Post-initialized 'A' = Available 'D' = Disabled 'E' = Errored

	| State     | ID                   | Version           | Source                                        | Signature                                |
	|:--------- |:-------------------- |:----------------- |:--------------------------------------------- |:---------------------------------------- |
	| UCHIJAAAA | minecraft            | 1.12.2            | minecraft.jar                                 | None                                     |
	| UCHIJAAAA | mcp                  | 9.42              | minecraft.jar                                 | None                                     |
	| UCHIJAAAA | FML                  | 8.0.99.99         | forge-1.12.2-14.23.2.2654.jar                 | e3c3d50c7c986df74c645c0ac54639741c90a557 |
	| UCHIJAAAA | forge                | 14.23.2.2654      | forge-1.12.2-14.23.2.2654.jar                 | e3c3d50c7c986df74c645c0ac54639741c90a557 |
	| UCHIJAAAA | thedragonlib         | 1.12.2-5.2.0      | thedragonlib-1.12.2-5.2.0.jar                 | None                                     |
	| UCHIJAAAA | armorplus            | 1.12.2-11.13.0.40 | armorplus-1.12.2-11.13.0.40.jar               | None                                     |
	| UCHIJAAAA | quark                | r1.4-123          | Quark-r1.4-123.jar                            | None                                     |
	| UCHIJAAAA | autoreglib           | 1.3-16            | AutoRegLib-1.3-16.jar                         | None                                     |
	| UCHIJAAAA | backpacks16840       | 3.4.4             | backpacks+1.12.2+-+3.4.4.jar                  | None                                     |
	| UCHIJAAAA | baubles              | 1.5.2             | Baubles-1.12-1.5.2.jar                        | None                                     |
	| UCHIJAAAA | betterfoliage        | 2.1.10            | BetterFoliage-MC1.12-2.1.10.jar               | None                                     |
	| UCHIJAAAA | biomesoplenty        | 7.0.1.2386        | BiomesOPlenty-1.12.2-7.0.1.2386-universal.jar | None                                     |
	| UCHIJAAAA | ceramics             | 1.12-1.3.4        | Ceramics-1.12-1.3.4.jar                       | None                                     |
	| UCHIJAAAA | colytra              | 1.0.4.2           | colytra-1.12.2-1.0.4.2.jar                    | 5d5b8aee896a4f5ea3f3114784742662a67ad32f |
	| UCHIJAAAA | craftablehorsearmour | 1.3               | CraftableHorseArmour-1.3.0-1.12.jar           | None                                     |
	| UCHIJAAAA | jei                  | 4.8.5.159         | jei_1.12.2-4.8.5.159.jar                      | None                                     |
	| UCHIJAAAA | cyclicmagic          | 1.14.0            | Cyclic-1.12.2-1.14.0.jar                      | None                                     |
	| UCHIJAAAA | dailies              | 1.12.2-6          | dailies-1.12.2-6.jar                          | None                                     |
	| UCHIJAAAA | familiarfauna        | 1.0.9             | FamiliarFauna-1.12.2-1.0.9.jar                | None                                     |
	| UCHIJAAAA | findercompass        | 1.12              | FinderCompass-1.12.1.jar                      | None                                     |
	| UCHIJAAAA | floricraft           | 4.4.1             | Floricraft-1.12.2-4.4.1.jar                   | None                                     |
	| UCHIJAAAA | forgelin             | 1.6.0             | Forgelin-1.6.0.jar                            | None                                     |
	| UCHIJAAAA | globalgamerules      | 2.1               | GlobalGameRules-1.12-2.1.6.jar                | None                                     |
	| UCHIJAAAA | infernalmobs         | 1.7.5             | InfernalMobs-1.12.2.jar                       | None                                     |
	| UCHIJAAAA | ironchest            | 1.12.2-7.0.40.824 | ironchest-1.12.2-7.0.40.824.jar               | None                                     |
	| UCHIJAAAA | journeymap           | 1.12.2-5.5.2      | journeymap-1.12.2-5.5.2.jar                   | None                                     |
	| UCHIJAAAA | lootbags             | 2.5.4b            | LootBags-1.12.2-2.5.4b.jar                    | None                                     |
	| UCHIJAAAA | moreplayermodels     | 1.12.2            | MorePlayerModels_1.12.2(18jan18).jar          | None                                     |
	| UCHIJAAAA | multimine            | 1.5.8             | MultiMine-1.12.2.jar                          | None                                     |
	| UCHIJAAAA | harvestcraft         | 1.12.2t           | Pam's+HarvestCraft+1.12.2t.jar                | None                                     |
	| UCHIJAAAA | roguelike            | 1.8.0             | RoguelikeDungeons-1.12.2-1.8.0.jar            | None                                     |
	| UCHIJAAAA | ruins                | 17.0              | Ruins-1.12.2.jar                              | None                                     |
	| UCHIJAAAA | soundfilters         | 0.10_for_1.12     | SoundFilters-0.10_for_1.12.jar                | None                                     |
	| UCHIJAAAA | twilightforest       | 3.4.239           | twilightforest-1.12.2-3.4.239-universal.jar   | None                                     |
	| UCHIJAAAA | variedcommodities    | 1.12.2            | VariedCommodities_1.12.2(15may18.jar          | None                                     |

	Loaded coremods (and transformers): 
ColytraLoadingPlugin (colytra-1.12.2-1.0.4.2.jar)
  c4.colytra.core.asm.ElytraTransformer
ForgelinPlugin (Forgelin-1.6.0.jar)
  
MMFMLCorePlugin (MultiMine-1.12.2.jar)
  atomicstryker.multimine.common.fmlmagic.MMTransformer
BCModPlugin (backpacks+1.12.2+-+3.4.4.jar)
  brad16840.core.ClassTransformer
LoadingPlugin (Quark-r1.4-123.jar)
  vazkii.quark.base.asm.ClassTransformer
FCFMLCorePlugin (FinderCompass-1.12.1.jar)
  atomicstryker.findercompass.client.coremod.FCTransformer
BetterFoliageLoader (BetterFoliage-MC1.12-2.1.10.jar)
  mods.betterfoliage.loader.BetterFoliageTransformer
	GL info: ~~ERROR~~ RuntimeException: No OpenGL context found in the current thread.
	Profiler Position: N/A (disabled)
	Player Count: 1 / 8; [EntityPlayerMP['Iteries'/134, l='Wastrik', x=177.33, y=32.00, z=-1280.27]]
	Type: Integrated Server (map_client.txt)
	Is Modded: Definitely; Client brand changed to 'fml,forge'
	OptiFine Version: OptiFine_1.12.2_HD_U_D1
	OptiFine Build: 20180323-135452
	Render Distance Chunks: 12
	Mipmaps: 4
	Anisotropic Filtering: 1
	Antialiasing: 0
	Multitexture: false
	Shaders: null
	OpenGlVersion: 4.6.0 NVIDIA 391.35
	OpenGlRenderer: GeForce GTX 750 Ti/PCIe/SSE2
	OpenGlVendor: NVIDIA Corporation
	CpuCount: 4
