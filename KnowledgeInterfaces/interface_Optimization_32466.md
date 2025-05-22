# Optimization (Object)

**_Represents an Optimization object._**

## Properties

### Property **AlgorithmType**( ) As [CatAlgorithmType](../KnowledgeInterfaces/enum_CatAlgorithmType_54838.md)

Returns or sets the algorithm type. Currently available algorithms are gradient and simulatedAnnealing

**See also:**      [CatAlgorithmType](../KnowledgeInterfaces/enum_CatAlgorithmType_54838.md) 
### Property **Constraints**( ) As [CATIAOptimizationConstraints](../KnowledgeInterfaces/interface_OptimizationConstraints_116449.md) (Read Only)

Returns the collection of optimization constraints.  
### Property **ConvSpeed**( ) As long

Returns or sets the convergence speed for some gradients and the simulated annealing.  
### Property **FreeParameters**( ) As [CATIAFreeParameters](../KnowledgeInterfaces/interface_FreeParameters_42284.md) (Read Only)

Returns the collection of the free parameters.  
### Property **MaxEvalsNb**( ) As long

Returns or sets the maximum number of model updates allowed during one run of the optimization.  
### Property **MaxEvalsWoImprovement**( ) As long

Returns or sets the maximum number of model updates without improvement of the problem solution during one run of the optimization.  
### Property **MaxTime**( ) As long

Returns or sets the maximum time allowed for one run of the optimization (in minutes).  
### Property **ObjectiveParameter**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md)

Returns or sets the objective parameter of the optimization. This parameter can not exist (in this case the get_ method returns E_FAIL) when the optimization contains only constraints and uses Simulated Annealing, or if the optimization feature doesn't contain all information necessary to be run.  
### Property **OptimizationType**( ) As [CatOptimizationType](../KnowledgeInterfaces/enum_CatOptimizationType_78349.md)

Returns or sets the type of the optimization: minimum, maximum or target value searched on the objective parameter.

**See also:**      [CatOptimizationType](../KnowledgeInterfaces/enum_CatOptimizationType_78349.md) 
### Property **TargetValue**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) (Read Only)

Returns the objective parameter target value. (used only if the optimization type is a target value search)  
### Property **UseMaxEvalsWoImprovement**( ) As boolean

Returns or sets if the number of updates without improvement of the solution has to be used as a termination criterion.  
### Property **UseMaxTime**( ) As boolean

Returns or sets if max time has to be used as a termination criterion.  Methods

### Sub **Run**( boolean  `iWithStopDialog`)

Runs the optimization as it is defined. The stop dialog appears if argument is TRUE
Before running, a check is made to ensure that the optimization feature contains enough information to run the optimization. In the case where some information is missing, this method returns E_FAIL
WARNING : if argument is TRUE, the optimization is launched asynchronously, and you can not run several optimizations in this mode.