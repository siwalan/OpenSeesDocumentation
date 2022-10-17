.. _Mass:

Mass Command
-------------------

This command is used to set the mass at a node. 

.. function:: mass $nodeTag (ndf $massValues) 

.. list-table:: 
   :widths: 10 10 40
   :header-rows: 1

   * - Argument
     - Type
     - Description
   * - $nodeTag
     - |integer|
     - integer tag identifying node whose mass is set 
   * - $massValues
     - |float|
     - ndf nodal mass values corresponding to each DOF

.. admonition:: Example:


   1. **Tcl Code**

   .. code-block:: tcl

        mass 2 2.5 0.0 2.5 0.0 0.0 0.0; # define mass in x (ndf=1) and z (ndf=3) coordinates and assigning zero mass at other DOFs (Y-dir and rotational mass.) 


Code Developed by: |fmk|
