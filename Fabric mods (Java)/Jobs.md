# Envoys
## Description
This mod was designed to allow players on the server to do normal activities and earn ingame currency for them. The player had to select a job, and once a task had been completed (such as them mining coal), the mod gave them some currency for that. If the "miner" job hadn't been selected, no currency would be given. Storage was done with databases (MongoDB) so the player would get to keep their job selections even when the server restarts. Lots of mixins had to be used to determine when an action had been completed; especially with fishing, as there is no natural listener for the event that I wanted. 