sudoku
======
This is a maven project created from eclipse vaadin-archetype-application was used.
Maven install can be done to compile this project
and to run it use tomcat 7 and connect from browser using localhost:8080/sudo

This app solves the sudoku puzzle. no issues there.

However,
Table cells are not getting updated as the data is changing behind the scene.
The entire table is getting updated at the end of execution of the program. But I want to see each 
number change real time as I assign a value to each cell. Any code help is really appreciated.


I was under the impression that doing this on container

Item row = container.getItem(cell.getRowIndex());
Property<Integer> col = row.getItemProperty(cell.getColumnIndex());
col.setValue(num);

will update the table automatically. but doesn't work

I even tried 
  	((IndexedContainer) container).addValueChangeListener(new ValueChangeListener() {
adding a valuechangelistener but this is giving me another error 
StackOverFlow exception on line 114   			// item.getItemProperty(propertyId).setValue(value);
which I commented out. (Look in MyVaadinUI.java)

Basically, I am initialzing the container data with 0's in   
createContainerData()
Then populating the table when a click is done on the button "Populate"
call to uploadReceiver.getMatrix() will get the matrix[][] which is two dim array of integers.

My Email for any details: sbollap1@gmail.com
