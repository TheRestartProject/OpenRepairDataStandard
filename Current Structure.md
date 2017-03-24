# Current Structure

This represents the current data points we are recording in our Fixometer application.  Note: this doesn't represent the full data schema of the Fixometer application - e.g. some internal tables such as users are not recorded here.  See the [Fixometer](https://github.com/therestartproject/fixometer) project for more information.

The structure here is provided as reference for a starting point to the open standard.  As we move to an open data standard, things such as the types of data and whether certain data is required vs optional will change.

## categories

Devices are grouped into categories.  The category also acts as a proxy for the carbon footprint and waste weight measures.  
Each category contains data on the average weight, data on how repaired devices displace new devices, and on the carbon footprint to manufacture each type of electrical device.

* `idcategories`: unique identifier.
* `name`: category name.
* `weight`: average weight. 
* `footprint`: 
* `footprint_reliability`: metric for the reliability of the data.  
* `lifecycle`: 
* `lifecycle_reliability`: 
* `extended_lifecycle`: 
* `extended_lifecycle_reliability`: 
* `revision`: 
* `cluster`: id of the cluster that this category is associated with.

## clusters

The device categories fit in to four clusters: computers and home office, electronic gadgets, home entertainment, kitchen and household items.

* `idclusters`: unique identifier.
* `name`: name of the cluster.

## devices

Devices are the items that are brought to events to be fixed.  Various characteristics of the device are recorded, and the outcome of the attempted repair is also recorded.

* `iddevices`: unique identifier.
* `event`: The event that the device has been recorded at.
* `category`: The category that the device is part of.
* `category_creation`: 
* `estimate`: 
* `brand`: A description of the manufactuer of the device.  
* `model`: A description of the model.  
* `problem`:  What is the problem?
* `spare_parts`: Whether or not spare parts are needed as part of the fix.
* `repair_status`: Whether it was fixed, repairable, or end-of-life. 
* `professional_help`: When a device is repairable, whether it requires a professional repairer 
* `more_time_needed`: When a device is repairable, whether it requires more time at a future community event
* `do_it_yourself`: When a device is repairable, whether the repair can be completed by the owner 
* `repaired_by`: Volunteer who led the repair (currently not active)
* `created_at`: internal audit trail purposes.
* `modified_at`: internal audit trail purposes.

## events

Devices are brought for repair to events.  At an event, multiple devices are logged.

* `idevents`: unique identifier.
* `group`: foreign key to the group this event is part of.
* `event_date`: date of the event.  
* `start`: start time of the event.
* `end`: end time of the event.
* `location`: textual description of where the event is taking place.
* `latitude`: geocoded latitude
* `longitude`: geocoded longitude
* `free_text`: textual description of the event
* `pax`: number of participants that attended the event
* `volunteers`: number of volunteers
* `hours`:   number of hours volunteered
* `wordpress_post_id`: link to the corresponding post on Wordpress for the event
* `created_at`: internal audit trail.  
* `modified_at`: internal audit trail. 

## groups

A group hosts the events that devices are brought to for repair.

* `idgroups`: unique identifier.
* `name`: the group's name.
* `location`: 
* `longitude`: geocoded longitude
* `latitude`: geocoded latitude
* `area`: 
* `frequency`: 
* `free_text`: 
* `wordpress_post_id`:
