icon:: 🪄
exclude-from-graph-view:: true

-
- ## Additional Information
  template:: Additional Information
  template-including-parent:: false
	- **Description**:
	- **Also known as (these names are not encouraged)**:
-
- ## Entity
  template:: Entity
  template-including-parent:: false
	- type:: entity
	- **Attributes**
		- PetId
		- Name
	- **Behaviors**
		- UpdateVaccinationRecord([[Vaccination]])
		- ScheduleAppointment([[AppointmentDetails]])
-
- ## Value Object
  template:: Value Object
  template-including-parent:: false
	- type:: value-object
	- **Attributes**
		- Date
		- Time
		- Reason
-
- ## Aggregate Root
  template:: Aggregate Root
  template-including-parent:: false
	- type:: aggregate-root
	- *Includes*
		- [[Pet]]
		- List< [[Vaccination]] >
		- List<[[Appointment]]>
	- **Behaviors**
		- AddVaccination([[Vaccination]])
-
- ## Repository
  template:: Repository
  template-including-parent:: false
	- type:: repository
	- **Behaviors**
		- FindById(PetId)
-
- ## Domain Events
  template:: Domain Event
  template-including-parent:: false
	- type:: domain-event
	- **Attributes**
		- AppointmentId
		- Date
		- PetId
-
- ## Service
  template:: Service
  template-including-parent:: false
	- type:: service
	- **Behaviors**
		- ScheduleAppointment(PetId, Vaccination)