This module is for the Drupal 8 Immersion course.

To use this module you must follow the instructions given in the file:
"/config/install/migrate_plus.migration.migrate_csv.yml"


Notice that you will need to move the "movies.csv" file to the
appropriate location.
The location is indicated on line 43 of the above mentioned file.

Migrations are essentially defined in three phases:
1) Source: Starting at line 39, the type of source is defined (CSV in our case)
  The "column_names:" indicate the columns of the CSV. Notice how the column_names are referenced
  in the Process phase.

2) Process: Starting at line 73, the source data is modified (or not) in accordance to the process plugin.
   After processing the source data according to the plugin, the data is ultimately stored in the defined fields.

3) Destination: Starting at line 139, the processed data is stored according to the specifications set here.
   In this case, the plugin used is "entity:node" which means migration will create nodes (i.e. content entities) of type 'movie'
   as defined on lines 75, 76, 77 of the Process phase.
