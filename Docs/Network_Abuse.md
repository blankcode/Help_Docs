# Dealing with people abusing the network:

## Users on my network are abusing it and harming the expierience of other users / servers / mission critical services

In this use case, a developent department is regularly updating a large amount of data in a database every few minutes. This was litterally crippling the Admin's network.

### Answer Begins:

**Make them stop.** They are compremising the integrity of the network and causing frequent/major outages for the rest of the company.

    "You are abusing the network, change your methods or your devices will be banned."

Then when they complain, because you know they will...

### We can solve this a few ways:

- **Note:** Any and all hardware needs will come from the \$[Offending_Party's] budget, not IT's.
- Upgrade the bulk of the network to 10Gbit.
  - Or even 20-40, talking multiple 10G and just the backbones if needed.
- Make the DB server local to the Devs only, with direct links to the DB.
  - Don't let it go through anyone else's switches.
  - Again a sprinkling of 10Gbit can smooth relations with the offenders.
  - There are plenty of low cost 10GB over Copper solutions out there now.
- Change the software to not pull so much data so often.
  - Change to a Delta Replication (Changes Only) model to the software, rather than copying and replacing the entire file(s).
