=====================================
 <name of application> specification
=====================================

Designing the application
-------------------------

With our specification in hand and our requirements clear, it's time to start 
designing our solution. The main focus of our application is the data entry forma 
itself, so we'll begin with that GUI component.

We're going to create a basic design for our form in three steps:

  1. Determine the appropriate input widget type for each data field.
  2. Group together related items to create a sense of organization.
  3. Lay out our widgets within their groups.

Deciding on input widgets
-------------------------

Without committing ourselves to a particular GUI library or widget set, we can 
start our form design by deciding on an appropriate input widget type for each 
field. Most toolkits come with the same basic types of inputs for different 
types of data.

+------------------+-------------------+------------------------+
|Widget type       |Tkinter example    |Used for                |
+============+=====+===================+========================+
|                  |                   |                        |
+------------------+-------------------+------------------------+

Grouping our fields
-------------------

Humans tends to be confused when staring att a huge wall of inputs in no 
particular order. You can do your users a big favor by breaking up the input 
form into into sets of related fields. Of course, that assumes that your data 
has related sets of fields.

  * Perhaps Age, Last name, First name, ..., could be grouped under 'personal data'
  * ...

Most GUI libraries offer a variety of ways to group sections of a form together.

  * Tabs (notebook)
    - Allows multiple tabbed pages that the user can switch between.
  * Frames/boxes
    - Draws boxes around sections of a form, sometimes with a header.
  * Accordion
    - Divides a form into sections that can be hidden or expanded one at a 
      time.

Laying out the form
-------------------

So far, we know we have n inputs, which are grouped as follows:

  * n fields under 'personal data'
  * ...

Take a moment to think of the grid layout and make a mockup for the form.

Laying out the application
--------------------------

With your form designed, it's time to consider the rest of the applications 
GUI:

  * What buttons is needed? Save button, reset button?
  * Status bar?
  * Header, footer?

Evaluting technology options
----------------------------

Let's evalute the application according to these criterias:

  * Performance:
    - Will this be a high-performance application?
    - Are there computationally demanding tasks?
    - Is high speed critical?
    - Will Python and Tkinter work in terms on performance?
  * Features availability:
    - Meet the front-end requirements?
    - Meet the back-end requirements?
  * Cost and license:
    - Will the project be distributed?
    - Will the project be sold?
    - License conserns?
    - Budget for the project?
    - Python and Tkinter are free and liberally licensed.
  * Platform support:
    - Which operating system do you develop the application on?
    - Which operating system should the application be run on?
  * Developer knowledge and confidence:
    - Front-end experience?
    - Back-end experience?
