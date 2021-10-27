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
	ignition_factor_primary
	ignition_factor_secondary
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
	DimBattalion
	DimAction
	DimSituation
	DimPropertyUse
	DimAreaOfFireOrigin
	DimDistrict
	
## Assumptions
	- Only these dimensions are the only dimensions available to be designed
	- The Dataset changes its content once a day
