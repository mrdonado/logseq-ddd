## Scenario 1
	- Imagine a pet owner brings their pet to the clinic for a vaccination. The process involves several DDD concepts:
	- **[[PetRecord]]** is retrieved from the **[[PetRepository]]** using the pet's identity.
	- A **[[Vaccination]]** value object is created with the vaccination details.
	- The vaccination is added to the **[[PetRecord]]**, leveraging an **Aggregate Root** to ensure the operation's integrity.
	- A **[[VaccinationUpdated]]** domain event is published to possibly trigger other side effects, such as notifying the owner.
	- The updated **[[PetRecord]]** is persisted back to the **[[PetRepository]]**.