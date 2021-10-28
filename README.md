# AZSynapseTests

This is a Data Warehouse projects of Fire Incidents from the Public SF Gov Data

## The dataset contains the following columns:
	incident_number
	exposure_number
	id
	address
	incident_date
	call_number
	alarm_dttm
	arrival_dttm
	close_dttm
	city
	zipcode
	battalion_id_fk
	station_area
	box
	suppression_units
	suppression_personnel
	ems_units
	ems_personnel
	other_units
	other_personnel
	first_unit_on_scene
	estimated_property_loss
	estimated_contents_loss
	fire_fatalities
	fire_injuries
	civilian_fatalities
	civilian_injuries
	number_of_alarms
	primary_situation
	mutual_aid
	action_taken_primary
	action_taken_secondary
	action_taken_other
	detector_alerted_occupants
	property_use
	area_of_fire_origin
	ignition_cause
	ignition_factor_primary_id_fk
	ignition_factor_secondary_id_fk
	heat_source
	item_first_ignited
	human_factors_associated_with_ignition
	structure_type
	structure_status
	floor_of_fire_origin
	fire_spread
	no_flame_spead
	number_of_floors_with_minimum_damage
	number_of_floors_with_significant_damage
	number_of_floors_with_heavy_damage
	number_of_floors_with_extreme_damage
	detectors_present
	detector_type
	detector_operation
	detector_effectiveness
	detector_failure_reason
	automatic_extinguishing_system_present
	automatic_extinguishing_sytem_type
	automatic_extinguishing_sytem_perfomance
	automatic_extinguishing_sytem_failure_reason
	number_of_sprinkler_heads_operating
	supervisor_district
	neighborhood_district

## Dimensions: These are the dimensions stablished to match some Fact columns and expand its data
	DimBattalion: Contains Action Data for 'battalion_id_fk'.
	DimAction: Contains Action Data for 'action_taken_primary_id_fk' & 'action_taken_secondary_id_fk'.
	DimSituation: Contains Action Data for 'primary_situation_id_fk'.
	DimPropertyUse: Contains Action Data for 'property_use_id_fk'.
	DimAreaOfFireOrigin: Contains Action Data for 'area_of_fire_origin_id_fk'.
	DimDistrict: Contains Action Data for 'supervisor_district_id_f'k & neighborhood_district_id_fk'.
	
## Assumptions
	- Only these dimensions are the only dimensions available to be designed
	- The Dataset changes its content once a day

## Steps:
	1. Create the Azure Resource Group.
	2. Add the Synapse Analytics service to the RG.
	3. Inside Synapse: create Apache Spark and SQL Pool
	4. Create a new Repository to store all your commits and attach it to your current Synapse instance.
	5. Create a new Branch and Make sure that all commits are working great.
	6. Explore how the API Data looks like.
	7. Create the pipeline in the "integrate" section to retrieve the Data from Fire Incidents API and load it into a SQL Pool table (Without transformations)
	8. Create the CREATE statements for all DIM and FACT tables
	9. Prepare each Merge statement capable of loading and updating the data into DIM and FACT tables.
	10. Store that set of scripts into a Stored Procedure.
	11. Add the Stored Procedure to the Integration Pipeline.
	12. Set up a trigger to run in a daily bases.
	13. Debug all your solution and make it work!
	
### Future Steps
	- Improve the SP performance by adding indexes and temp tables
	- Improve the DW schema so all entities relate to the FACT table and the architecture gets better.
	- Create some PySpark scripts to analyze the data in a Dataframe
	
	
