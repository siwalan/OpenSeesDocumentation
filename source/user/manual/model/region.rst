.. _region:

Region Command
-------------------

The region command is used to label a group of nodes and elements. This command is also used to assign rayleigh damping parameters to the nodes and elements in this region. The region is specified by either elements or nodes, not both. If elements are defined, the region includes these elements and the all connected nodes, unless the -eleOnly option is used in which case only elements are included. If nodes are specified, the region includes these nodes and all elements of which all nodes are prescribed to be in the region, unless the -nodeOnly option is used in which case only the nodes are included. 

.. function::  region $regTag <-ele ($ele1 $ele2 ...)> <-eleOnly ($ele1 $ele2 ...)> <-eleRange $startEle $endEle> <-eleOnlyRange $startEle $endEle> <-node ($node1 $node2 ...)> <-nodeOnly ($node1 $node2 ...)> <-nodeRange $startNode $endNode> <-nodeOnlyRange $startNode $endNode> <-node all> <-rayleigh $alphaM $betaK $betaKinit $betaKcomm> 

.. list-table:: 
   :widths: 10 10 40
   :header-rows: 1

   * - Argument
     - Type
     - Description
   * - $regTag
     - |integer|
     - unique integer tag 
   * - $ele1 $ele2
     - |integer|
     - tags of selected elements in domain to be included in region (optional, default: omitted) 
   * - $node1 $node2 ...
     - |integer|
     - tags of selected nodes in domain to be included in region (optional, default: omitted) 
   * - $startEle $endEle
     - |integer|
     - tag for start and end elements -- range of selected elements in domain
   * - $alphaM $betaK $betaKinit $betaKcomm
     - |integer|
     - Arguments to define Rayleigh damping matrix (optional, default: zero) 

.. note:: 
    * The user cannot prescribe the region by BOTH elements and nodes. 
  

.. admonition:: Example:


   1. **Tcl Code**

   .. code-block:: tcl

        region 1 -ele 1 5 -eleRange 10 15

        region 2 -node 2 4 6 -nodeRange 9 12 

Code Developed by: |fmk|
