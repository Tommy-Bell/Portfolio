# Envoys
## Description
This mod's concept was pretty simple, yet it wasn't so simple to make. The idea was to create a minecraft chest to randomly spawn in a specified area (defined in config json) in the world. The chest would give a random reward upon being right clicked. Making this was quite simple, but I did face a pretty big issue; lag. Unforutunately, placing the chest created a large amount of lag. After a lot of diagnosing, I discovered it was upon first loading the chunk that the chest was to be spawned in. Loading in so much data caused a large lag spike, and changing threads didn't help with it.
<br />
<br />
After a lot of research, I managed to find [documentation](https://maven.fabricmc.net/docs/yarn-1.16.4+build.1/net/minecraft/server/world/ServerChunkManager.html#addTicket-net.minecraft.server.world.ChunkTicketType-net.minecraft.util.math.ChunkPos-int-T-) about an add ticket function of the chunk manager. This meant that the placement code could be delayed until the chunk was loaded when the server next can load it.
