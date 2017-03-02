# Current Structure

This represents the current data points we are recording in our Fixometer application.  This doesn't represent the full data schema of the Fixometer application - e.g. some internal tables such as users are not recorded here.  

## categories

* `idcategories`: unique identifier.
* `name`: category name.
* `weight`: 
* `footprint`: 
* `footprint_reliability`: metric for the reliability of the data.  
* `lifecycle`: 
* `lifecycle_reliability`: 
* `extended_lifecycle`: 
* `extended_lifecycle_reliability`: 
* `revision`: 
* `cluster`: id of the cluster that this category is associated with.

## clusters

* `idclusters`: unique identifier.
* `name`: name of the cluster.

## devices

* `iddevices`: unique identifier.
* `event`: The event that the device has been recorded at.
* `category`: The category that the device is part of.
* `category_creation`: 
* `estimate`: what is this varchar?
* `brand`: A description of the manufactuer of the device.  
* `model`: A description of the model.  
* `problem`:  What is the problem?
* `spare_parts`: Whether or not spare parts are needed as part of the fix.
* `repair_status`: Whether it was fixed, repairable, or end-of-life. 
* `professional_help`: 
* `more_time_needed`: 
* `do_it_yourself`: 
* `repaired_by`: do we record this in the interface?
* `created_at`: internal audit trail purposes.
* `modified_at`: internal audit trail purposes.

## events

* `idevents`: unique identifier.
* `group`: foreign key to the group this event is part of.
* `event_date`: date of the event.  
* `start`: start time of the event.
* `end`: end time of the event.
* `location`: textual description of where the event is taking place.
* `latitude`: geocoded latitude
* `longitude`: geocoded longitude
* `free_text`: textual description of the event? 
* `pax`: what is this?
* `volunteers`: number of participants?  
* `hours`: number of hours that the event lasted?  
* `wordpress_post_id`: link to the corresponding post on Wordpress for the event.
* `created_at`: internal audit trail.  
* `modified_at`: internal audit trail. 

## groups

* `idgroups`: unique identifier.
* `name`: the group's name.
* `location`: 
* `longitude`: geocoded longitude
* `latitude`: geocoded latitude
* `area`: 
* `frequency`: 
* `free_text`: 
* `wordpress_post_id`:
