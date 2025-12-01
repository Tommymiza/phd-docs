# Summary of the Multi-Agent Modeling Guide "Firefighters"

## Context and Nature of the Model

The "Firefighters" model is a simplified pedagogical model designed for learning agent-based modeling and simulation (ABMS). It is a benchmark model created for students or researchers wishing to understand the basic principles of ABMS, without the aim of providing real decision-support.

## 1. Model Framework

### 1.1. Objective

The model serves as an educational tool to allow users to manipulate a simple multi-agent model. Users must conceptualize, formalize, implement, and simulate the model, then discuss the management issues addressed.

### 1.2. Model Scenario

The modeled system represents a 900-hectare forest landscape susceptible to fires, divided into 1-hectare plots. The initial landscape is randomly composed of 50% forested plots and 50% cleared plots. When a fire breaks out, it spreads to neighboring forested plots.

**The firefighters**: A brigade of 10 volunteer firefighters monitors the forest. Each firefighter patrols by moving randomly from plot to plot. When they detect a nearby fire, they move to extinguish it.

**Two scenarios are studied**:

1. **Without coordination**: Firefighters act independently, without knowing the position or activity of others
2. **With coordination**: Each firefighter knows the location and status of others. If they don't detect a nearby fire, they head toward the nearest fire being fought by a colleague

**Research objective**: Understanding under what conditions (number of firefighters, coordination skills) the brigade improves its effectiveness, measured by the total burned area and the time needed to extinguish the fire.

## 2. Structure and Initialization

### 2.1. Identified Entities and Attributes

**Firefighters**

- Scale: Elementary social entity
- Attributes: Status (patrolling or fighting fire), communication capability (yes/no)
- Relations: Fight fire, monitor landscape, communicate with each other

**Brigade**

- Scale: Group of 10 firefighters
- Relation: Composed of 10 firefighters

**Plots**

- Scale: Elementary spatial entity of 1 ha
- Attributes: State (forest, cleared, or on fire), area
- Relations: Neighboring relationship with other plots

**Landscape**

- Scale: 30 × 30 grid of plots
- Relation: Composed of plots

**Fire**

- Scale: Aggregate of plots on fire
- Attributes: Area
- Relations: Breaks out and spreads on plots

### 2.2. Initialization

**Space**:

- 900 plots of 1 ha
- Random configuration: 50% forest, 50% cleared
- Initial fire on 1 random forested plot

**Entities**:

- 1 brigade of 10 firefighters
- Initial location: Each firefighter placed randomly in the landscape (simulating the moment when the fire breaks out while firefighters are patrolling)

This guide illustrates the methodology for designing a multi-agent model, from describing the reference system to its formalization, including the identification of entities, attributes, and relations.
