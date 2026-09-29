# How should we model a ship colliding with a floating wind turbine?

**EMship Master’s thesis / research internship**  
*Investigation of ship structural modelling for collision analysis with floating offshore wind turbines*

What happens when a ship strikes an offshore wind turbine? Which structure deforms, where does the collision energy go, and how much detail do we need to reproduce the event in a numerical model?

This project invites a student to explore these questions using **LS-DYNA, Python and parametric modelling**. You will build ship models, run collision simulations and investigate which modelling choices make a meaningful difference to the results.

## From real collisions to numerical models

<p align="center">
  <img src="Media/01_ship-OWT_impact.gif" width="650" alt="Still images showing a vessel close to an offshore wind turbine during a collision sequence">
</p>

*Real-world collision imagery provides the context for the research. The supplied file is a still image.*

Our work so far has focused on the response of **deformable offshore wind turbine supports struck by a rigid ship**. This means the ship can move, but its structure cannot bend, buckle or crush. The turbine support is allowed to deform.

The numerical examples below illustrate the turbine response and the motion of the colliding bodies. Click a preview to open the corresponding MP4 video.

[![Ship–wind turbine collision simulation](Media/02_preview.png)](Media/02_media1_abhe.mp4)

*Collision simulation showing the interaction between a ship and a tubular wind turbine support.*

| View of the support | View of the ship motion |
|:---:|:---:|
| [![Support response during collision](Media/03_1_preview.png)](Media/03_1_Media1_John.mp4) | [![Ship motion during collision](Media/03_2_preview.png)](Media/03_2_Media2_John.mp4) |
| [Play video](Media/03_1_Media1_John.mp4) | [Play video](Media/03_2_Media2_John.mp4) |

<!-- Media slot 04: replace Media/04_image11_sarah.gif before displaying it. The supplied file contains a single black frame. -->

## But how realistic is a perfectly rigid ship?

Real ships can sustain substantial structural damage. Their hull plating and internal structure can deform and absorb part of the collision energy. A rigid-ship model cannot represent that contribution.

<p align="center">
  <img src="Media/05_1_Picture3.png" height="210" alt="Visible deformation of a red vessel's bow">
  <img src="Media/05_2_Picture4.png" height="210" alt="Damage to the side of a blue vessel">
  <img src="Media/05_3_Picture5.jpg" height="210" alt="Close view of damaged hull plating and exposed internal structure">
</p>

*Examples of ship structural damage. These photographs illustrate possible deformation; they are not presented as matched validation cases or as evidence that each incident involved a wind turbine.*

This leads to our next question: **when is the rigid-ship assumption sufficient, and when do we need to model ship deformation explicitly?** Answering it requires a practical way to generate and compare deformable ship models.

## The next step is the ship

We have developed simplified collision models and finite element studies of the turbine support, including work on its interaction with the surrounding water. The next stage is to investigate the ship structure with the same attention.

| Previous work: turbine deformation | → | This project: ship deformation |
|:---:|:---:|:---:|
| <img src="Media/06_1_ship_animation.gif" width="310" alt="Animation of a rigid ship interacting with a flexible turbine support"> | **Next step** | <img src="Media/06_2_def_ship_animation.gif" width="310" alt="Animation of a deformable ship impacting an idealised fixed rigid support"> |
| Rigid ship and deformable support | | Deformable ship and initially rigid support |

*Conceptual animations, not finite element results. The fixed support in the right-hand sketch is an idealised starting point for isolating ship deformation. Structural rigidity and floating-body motion are separate modelling choices: a rigid floating support may still translate and rotate.*

The initial comparisons will focus on the ship against an idealised rigid support. They will prepare the ship component for integration into the wider ship–floating wind turbine collision framework, and ultimately for studies in which both structures deform.

## What will you investigate?

The central question is **how detailed a ship model needs to be to capture the collision response at a reasonable computational cost**. The project will use controlled ship-like configurations; reproducing every detail of a particular vessel is not the starting requirement.

![Conceptual comparisons of ship structural detail, hull shape and hydrodynamic geometry](Illustrations/modelling_comparisons.svg)

*Illustrative modelling choices only. These sketches are not meshes, validated equivalent models or predicted results.*

Three possible comparisons will guide the study:

- **Structural detail:** compare an equivalent plate representation with panels in which the stiffeners are modelled explicitly. How does the choice affect deformation and the force required to crush the structure?
- **Hull shape:** compare a simple box-like geometry with a more representative curved hull. Which geometric features matter near the contact region?
- **Interaction with water:** where the coupled framework permits, compare simplified and more representative hull geometries for the hydrodynamic model. How much does that change the global motion and collision response?

The exact comparisons will be selected with the supervisors to keep the project manageable. Mesh sensitivity and consistent comparison conditions will help distinguish numerical effects from differences caused by the modelling assumptions.

## Your work during the thesis

1. **Explore the literature.** Review ship collision modelling, stiffened panels and impacts against tubular structures. Identify relevant published comparisons or benchmark cases where available.
2. **Build a parametric ship model.** Use Python to generate LS-DYNA models with adjustable geometry, plating and structural arrangements. Establish a working reference configuration before adding complexity.
3. **Prepare repeatable simulations.** Automate model preparation and extraction of the main results so that modelling choices can be compared systematically.
4. **Run a focused comparison study.** Examine deformation patterns, collision forces, absorbed energy and, where relevant, global motion. Compare simplified models with more detailed numerical references and suitable published cases.
5. **Explain the mechanics.** Identify why the results change and whether additional detail is worth the extra modelling and simulation time. Turn these findings into practical recommendations.

The wind turbine models and the existing coupling framework will be provided as a starting point. The student’s main responsibility will be the **ship modelling methodology and its assessment**.

## What will you gain?

You will gain experience in Python-based engineering automation, parametric model generation, nonlinear finite element analysis with LS-DYNA, and interpretation of structural collision behaviour. You will also learn to assess the limitations of a numerical model and communicate the evidence behind a modelling decision.

This project would suit a student who:

- enjoys structural mechanics and understanding how structures deform;
- has good Python programming skills and likes building reusable tools;
- is interested in numerical simulation and willing to learn LS-DYNA;
- enjoys checking results, testing assumptions and explaining physical behaviour.

## How the work continues

The thesis will deliver a reusable ship modelling procedure, a documented set of comparison simulations and recommendations on the required level of structural detail. These outputs will support wider collision studies and the future development of simplified analytical models of ship deformation within the ongoing PhD research.

The student will have an independent research question and will interpret their own comparison study. The subsequent large-scale simulation campaign and analytical model development form the longer-term research outlook.

## Interested?

**Research contact:** Gabriel Vandegar — University of Liège, ArGEnCo/ANAST.  
Contact and practical arrangements will be provided through the EMship topic proposal.
