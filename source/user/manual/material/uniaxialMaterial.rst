.. _uniaxialMaterial:

uniaxialMaterial Command
************************

This command is used to construct a uniaxial material, which provides a uniaxial stress-strain (or force-deformation) relationships.
. 

.. function:: uniaxialMaterial $matType $matTag $matArgs

.. csv-table:: 
   :header: "Argument", "Type", "Description"
   :widths: 10, 10, 40

   $matType, |string|,      material type
   $matTag,  |integer|,     unique material tag.
   $matArgs, |list|,        a list of material arguments with number dependent on material type


The following subsections contain information about **$matType** 

   .. toctree::
      :maxdepth: 3

      uniaxialMaterials/Steel/SteelList
      uniaxialMaterials/Concrete/ConcreteList
      uniaxialMaterials/Standard/StandardList
      uniaxialMaterials/Other/OtherList


