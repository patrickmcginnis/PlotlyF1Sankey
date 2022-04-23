This folder contains an html that links to the interactive sankey diagram, 
just open it in a browser to check it out.


If you would like to venture into the code and possibly run it here are some notes:

use pip to install plotly, (maybe use python3 command before pip if any issues, update pip?)
    pip install plotly==5.7.0

then just run the code
    python3 sankey.py

Notes:

Array for teams is size 13, some teams are blended where purchases were made and sponsor titles were changed
Array for drivers is size 68, drivers can be associated with multiple edges.

label field: 
    this is used for all the nodes, added the teams twice, inputs and outputs, as well as 2 extra fields,
    for retirement or rookies coming in.
    x, y, color, pad is just mapping for views

link is where magic happens:
    source: is all the source nodes where drivers are coming from. An initial setup is made for each team in 2011
    pulling each driver from the non affiliated field. Then each driver has all there source nodes(teams) mapped in this array.

    target: is all the target nodes where drivers are navigating towards.
    link: is the edge between the source and target
    customdata: is the driver data associated with the link, this pulls from the driver array and gives extra data.
