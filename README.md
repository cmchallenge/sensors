# Problem   1   -   Classifying   sensor   data
For   this   problem,   we   want   you   to   figure   out   how   containers   move   through   the   port   of   Oakland. Specifically,   we   want   to   track   3   events   that   happen   within   the   port:
1. When   the   container   is   unloaded   from   a   ship
2. When   the   container   is   loaded   onto   a   train
3. When   the   train   leaves   the   port

**For this problem, you can assume that every container will have all of these events and that   they happen in order.**

Let’s   say   we’ve   attached   a   couple   of   sensors   to   each   container:   SENSOR_A   and   SENSOR_B. Whenever   there   is   activity   for   a   specific   container,   we   receive   a   sensor   reading   from   both   of   its attached   sensors.   However,   there   is   a   lot   of   noise   associated   with   these   sensors.   Our   goal   is   to classify   these   sensor   readings   as   one   of   our   events   or   as   noise:
* UNLOAD_SHIP
* LOAD_TRAIN
* DEPART_TRAIN 
* NOISE

The   sensor   data   for   all   of   our   containers   is   contained   in   two   json   files:   train.json   and   test.json. The   structure   of   the   data   is   a  list  of  lists   of   dictionaries.   Each   inner   list   represents   one container’s   entire   sensor   history.   Each   dictionary   within   that   list   represents   a   specific   sensor reading.

Each   sensor   reading   dictionary   is   made   up   of   the   following   fields:
* TIME  :   (datetime)   the   time   that   the   sensor   reading   occurred
* SENSOR_A  :   (int)   the   sensor   A   measurement
* SENSOR_B  :   (int)   the   sensor   B   measurement
* LABEL  :   (str)   the   label   we   are   trying   to   classify

Your   goal   is   to   implement   a   model   that   predicts   the   value   of   field   ‘LABEL’   for   each   sample. Please   include   your   code,   any   analysis   you   performed,   and   share   your   thoughts   on   future   work.
