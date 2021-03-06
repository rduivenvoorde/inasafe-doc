.. _run-basic-inasafe:

Run Basic |project_name|
========================

**Learning Objectives:**

* Run |project_name| using flood and population models and examine the
  results
* Create an impact map
* Modify the threshold (parameters) of an impact function
* Run |project_name| using flood and building models and examine the results

**Data for this module**

Download the InaSAFEv2.0.zip from `InaSAFE Training Data Packages
<http://data.inasafe.org/TrainingDataPackages/>`_
or it will be provided to you during the training.

Introduction
------------

In this section we will run |project_name| using a scenario in Jakarta, Indonesia 
to determine the impact of a flood model on both Jakarta's population and buildings.

1. Go to :menuselection:`Project --> Open`.

2. If you have been working in QGIS previously a message box will appear 
   asking if you want to save the current project. Click :guilabel:`Discard`
   to exit your current work without saving.

.. image:: /static/training/socialisation/028_saveproject.*
   :align: center

3. Navigate to the :file:`InaSAFE_project` folder and 
   select :file:`Jakarta_floods.qgs`. Click :guilabel:`Open`.

The project looks something like this:

.. image:: /static/training/socialisation/029_jakartafloods.*
   :align: center


Number of population which need evacuation
------------------------------------------

The |project_name| panel has the first three drop-down menus
filled in already:

* A flood similar to the 2007 Jakarta event
* People
* Need evacuation

.. image:: /static/training/socialisation/030_showpeople.*
   :align: center

.. note:: The |project_name| panel may instead read as follows:
   
   * A flood similar to the 2007 Jakarta event
   * Buildings
   * Be flooded
   
   If so, click on buildings and change it to people. When you change this field,
   the impact function is automatically changed between :guilabel:`Be flooded`
   and :guilabel:`Need evacuation`, based on the combination of hazard and
   exposure layers.

4. Let's run this scenario first. Click :guilabel:`Run` in the lower 
   right corner of the |project_name| panel.

.. image:: /static/training/socialisation/031_run.png
   :align: center

A new layer should appear in the layer panel called :guilabel:`Population which
need evacuation`.

.. image:: /static/training/socialisation/032_results.*
   :align: center

In the |project_name| panel we now see text and statistics. The
details of this report are explained below.

.. image:: /static/training/socialisation/033_peoplefloodresult.*
   :align: center

**People:** |project_name| shows approximately how many people are located
in water deeper than one metre. It is assumed that all of these people will
need to evacuate their homes. The threshold of one metre can be changed
(see Changing threshold section below).

**Needs per week** is calculated using the above number of evacuated people to
estimate the amount of food, water and other products that the refugees will
need to survive. The default figures are based on Indonesian policy.

**Action checklist** is designed to make disaster managers think about what
they need to do to prepare for the event.

**Notes** explains the total people in the map canvas, the threshold of water
depth that requires evacuation and the source of the minimum needs assessment.

**Detailed gender and age report:** Statistical breakdown of the number of
females, minimum needs for women's hygiene and pregnant women, as
well as a statistical breakdown of Youth, Adults and Elderly.

Print Results
.............

5. Click :guilabel:`Print...` at the bottom of the |project_name| panel.

.. image:: /static/training/socialisation/034_print.*
   :align: center

.. note:: You can choose whether you want to print the whole analysis or just the current
   map extent. You can also pick an existing print template or you can navigate to your own
   QGIS template (.qpt). For more information about printing, click
   :guilabel:`Help` in the print window.

6. A window will pop up as shown below. Ensure that :guilabel:`Analysis extent`
   is selected under :guilabel:`Area to print` and :guilabel:`inasafe...` is chosen
   under :guilabel:`Template to use`. Click :guilabel:`Open PDF`.

.. image:: /static/training/socialisation/034a_impact_report.*
   :align: center

7. Navigate to where you would like to save the PDF
   and type :file:`Jakartaflood_evacuation_1m`. Click :guilabel:`Save`.

.. image:: /static/training/socialisation/034b_save_report.*
   :align: center

Two PDFs will be generated, which contain a map and a table of information about the impact.

.. image:: /static/training/socialisation/035_People_in_need_of_evacuation_1m.*
   :align: center

.. note:: In future versions of |project_name|, the developers will make improvements
   to the layout of these PDF files. *If you have time during this course please
   provide us with your ideas on how the print map and table should look!*

Changing threshold
..................

What if the disaster manager decides that people should be evacuated if they
are in 80cm or more of water? In this case we will need to change the water threshold
at which level people should be evacuated.

8. Click :guilabel:`Show question form` found at the top of the |project_name| panel.

.. image:: /static/training/socialisation/036_showquestion.*
   :align: center

9. To change the impact function click the :guilabel:`Options...` button next 
   to :guilabel:`Need evacuation`.

.. image:: /static/training/socialisation/037_functionchange.*
   :align: center

10. Type :kbd:`0.8` in the :guilabel:`Thresholds` field.

.. image:: /static/training/socialisation/038_configure.*
   :align: center

11. Click :guilabel:`OK`.

12. Click :guilabel:`Run` to process the scenario with the new water threshold.

.. image:: /static/training/socialisation/031_run.*
   :align: center

When the function completes, take a look at the new numbers
in the |project_name| panel. How have they changed?

.. todo:: How many people need to be evacuated?
   **Answer:** ______________________
   Is this the answer you were expecting?
   **Answer:** _____________________

13. Click :guilabel:`Print...` at the bottom the |project_name| panel.

.. image:: /static/training/socialisation/034_print.*
   :align: center

14. A window will pop up as shown below. Ensure that :guilabel:`Analysis extent` is
    selected under :guilabel:`Area to print` and :guilabel:`inasafe...` is chosen
    under :guilabel:`Template to use`. Click :guilabel:`Open PDF`.

.. image:: /static/training/socialisation/034a_impact_report.*
   :align: center

15. Navigate to where you would like to save the PDF and type 
    :file:`Jakartaflood_evacuation_80cm`. Click :guilabel:`Save`.

16. Next we will run the |project_name| analysis on buildings, but first let's turn 
    some layers off. In the Layers panel there should now be five layers. Uncheck 
    everything except:

    * A flood similar to the 2007 Jakarta event
    * Buildings

.. image:: /static/training/socialisation/039_buildingflood.*
   :align: center

Buildings Affected
------------------

17. Confirm that the |project_name| panel is set to query how many buildings
    might be flooded.

.. image:: /static/training/socialisation/040_inasafebuidlingflood.png
   :align: center

18. Notice that if you click on the drop-down list with :guilabel:`Buildings`,
    the people option is not available. This is because :guilabel:`people` 
    is not checked in the Layers panel.

.. note:: If you want to be able to select layers within the
   |project_name| panel that are not checked in the Layers panel you can
   modify the |project_name| options.
   For more information on |project_name| options, see the user documentation here: 
   :doc:`../../user-docs/application-help/options`.
   The options menu is also discussed later in this tutorial in :doc:`helpful_hints_and_tips`.

19. Click :guilabel:`Run` to process the new scenario.

.. image:: /static/training/socialisation/041_buildingfloodresults.png
   :align: center

In this scenario approximately 2,914 buildings could be affected out of 13,353
buildings. Your results may vary depending on updates that have been made to the
exposure data and the analysis extent.

.. note:: Due to the provincial BPBD work in OpenStreetMap, all important buildings 
   in this area have been mapped (and then some!).

   Important buildings are defined as:

   * Clinic/doctors
   * Fire stations
   * Government buildings
   * Hospitals
   * Places of worship
   * Police stations
   * Residential buildings
   * Schools
   * Sports facilities
   * Universities/colleges

In the |project_name| panel we now see text and statistics. The
details of this report are explained here:

**Action Checklist:** A different set of actions have been identified to
relate to structures.

**Note:** Similar to the last |project_name| analysis, this analysis also
assumes impact is in water above one metre.

**Detailed building type report:** This is a breakdown of important
infrastructure. When you choose to aggregate (we will do this later) this
table will show the number of buildings by aggregation boundary.

**Source** shows the source of the hazard and exposure datasets.


20. Click :guilabel:`Print...` at the bottom the |project_name| panel.

.. image:: /static/training/socialisation/034_print.png
   :align: center

21. A window will pop up as shown below. Ensure that :guilabel:`Analysis extent`
    is selected under :guilabel:`Area to print` and :guilabel:`inasafe...` is chosen
    under :guilabel:`Template to use`. Click :guilabel:`Open PDF`.

.. image:: /static/training/socialisation/034a_impact_report.*
   :align: center

22. Navigate to where you would like to save the PDF
    and type :file:`Jakartaflood_inundated_1m`. Click :guilabel:`Save`.


(Optional) Change the threshold to 0.8
......................................

You may try running this scenario again with a water threshold of 0.8 metres.

23. Check that |project_name| has the following in the drop-down boxes:

* A flood similar to the 2007 Jakarta event
* Buildings
* Be flooded

24. To change the impact function click the :guilabel:`Options...` button on 
    the |project_name| panel.

25. Type :kbd:`0.8` in the :guilabel:`Thresholds` field.

26. Click :guilabel:`Run` to process the scenario with the new water threshold.

27. Click :guilabel:`Print` and save PDFs the same way as before.

(Optional) Save your work
.........................

28. Click :menuselection:`Project --> Save` to save your current project

Because the InaSAFE output by default saved in temporary folder, you need to
manually save your InaSAFE output as new layer in same directiory as your project.

29. Right click on :guilabel:`Population which need evacuation` and click :guilabel:`Save As...`

30. A new window will appear. Click :guilabel:`Browse...` and name your new layer with
    :kbd:`Population which need evacuation`. Click :guilabel:`Save` and then click :guilabel:`OK`

:ref:`Go to next module --> <inasafe-in-more-detail>`
