# Aliste-Tech


**Electrician Allocation System:**
Let's say we have a system that manages electricians and the sites they need to work
on. The system helps ensure that the right electricians are sent to the right sites.
Here's a simple example:
**Input:**
- Electricians: 
 1. Electrician A (General)
 2. Electrician B (Grievance)
example: {
 name: 'Pranav', 
 phoneNumber: '6161232524', 
 zone: ['DELHI'], 
 grievanceElectrician: true 
 }, 
 { 
 name: 'Sidharth', 
 phoneNumber: '6161232524', 
 zone: [ 'NOIDA', 'GHAZIABAD' ], 
 grievanceElectrician: false 
 }, 
 
- Sites to be installed on a given day:
 1. Site X in City Noida (Grievance)
 2. Site Y in City Delhi (General)
example: y={
 name: 'KRISHNA ROY', 
 phone: '6163988877', 
 city: 'NOIDA', 
 AssignedElectritian: [], 
 InstallationDate: 2023-01-04T00:00:00.000Z, 
 grievance: false 
 }, 
 x={ 
 name: 'Anuj Gupta ', 
 phone: '6163988877', 
 city: 'DELHI', 
 AssignedElectritian: [], 
 InstallationDate: 2023-10-18T00:00:00.000Z, 
 grievance: true 
 } 
**Process:**
1. Give a button to automatically assign electricians to the sites.
2. When we click this button, the system works like this:
 - It first assigns the Grievance Electrician B to Site X because it's a grievance
site. Electrician B can handle grievances.
 - Then, it assigns Electrician A to site Y because he is a general electrician.
 - Each electrician is assigned to a maximum of three sites at a moment to keep 
things manageable.
 - You do not consider zone/city of electrician while handling the Grievance site 
and electrician as well
**Output:**
- After clicking the button:
 - Site X in City DELHI is assigned to Electrician B (Grievance).
 - Site Y in City NOIDA is assigned to Electrician A (General).
 
 y={
 name: 'KRISHNA ROY', 
 phone: '6163988877', 
 city: 'NOIDA', 
 AssignedElectritian: [ 
 {"electricianName": "Sidharth", 
"electricianAssignDate": "2023-10-25"}
 ],
 InstallationDate: 2023-01-04T00:00:00.000Z, 
 grievance: false 
 }, 
 x={ 
 name: 'Anuj Gupta ', 
 phone: '6163988877', 
 city: 'DELHI', 
 AssignedElectritian: [ 
 {"electricianName": "Pranav", 
"electricianAssignDate": "2023-10-25"}
 ],
 InstallationDate: 2023-10-18T00:00:00.000Z, 
 grievance: true 
 } 
In simple terms, this system ensures that:
- Grievance sites are handled by the Grievance electrician.
- General sites are distributed fairly among general electricians.
- No electrician is overwhelmed with too many sites to work on, that's why it is 
limited to three only.
- If any electrician is pending without site assignment and the site is also pending
then you can assign a grievance electrician to the general site or vice-versa. 
Rule to distribute electrician: number of sites on current date/number of available 
electricians on current date.
Things you have to do:
1. Give a page on the front end to change the installation date of the given
data(sites). 
2. Give a button on the page to auto-assign the site to the electrician 
based on the above rule. 
3. Show output on a new page or directly console the output.
