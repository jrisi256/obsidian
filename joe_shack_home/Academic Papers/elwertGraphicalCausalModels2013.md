---
type:
  - Chapter
author:
  - Felix Elwert
year: 2013
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Felix Elwert
* **Title**: Graphical Causal Models
* **Date of publication**: 2013
* **Pages**: 245-273
* **URL**: [https://doi.org/10.1007/978-94-007-6094-3_13](https://doi.org/10.1007/978-94-007-6094-3_13)
* **Tags**: #causal_inference, #comps_exam, #ds560, #graphical_causal_models
* **PDF Attachments**:
  * [elwertGraphicalCausalModels2013.pdf](zotero://open-pdf/library/items/BGVHXG7V)

## Abstract

This chapter discusses the use of [[directed acyclic graphs]] (DAGs) for causal inference in the observational social sciences. It focuses on DAGs’ main uses, discusses central principles, and gives applied examples. DAGs are visual representations of qualitative causal assumptions: They encode researchers’ beliefs about how the world works. Straightforward rules map these causal assumptions onto the associations and independencies in observable data. The two primary uses of DAGs are (1) determining the identifiability of causal effects from observed data and (2) deriving the testable implications of a causal model. Concepts covered in this chapter include identification, [[d-separation]], confounding, endogenous selection, and overcontrol. Illustrative applications then demonstrate that conditioning on variables at any stage in a causal process can induce as well as remove bias, that confounding is a fundamentally causal rather than an associational concept, that conventional approaches to causal mediation analysis are often biased, and that causal inference in social networks inherently faces endogenous selection bias. The chapter discusses several graphical criteria for the identification of causal effects of single, time-point treatments (including the famous backdoor criterion), as well identification criteria for multiple, time-varying treatments.

## Highlighted Notes

Causal identification and estimation are two different procedures. Causal identification is about identifying under what conditions association becomes causation or when does the observed correlation indicate a causal relationship rather than a spurious relationship. Estimating is finding a numerical estimate of what that effect actually is.

Specifying the appropriate statistical model to recover an effect that can be estimated is not a trivial task.

* [Go to annotation](zotero://open-pdf/library/items/BGVHXG7V?page=4&annotation=VPJGVVB7) “Identification analysis determines whether, and under which conditions, it is possible to strip an observed association of all its spurious components. We say that a causal effect is identified if a properly stripped association equals (“identifies”) the causal effect.” ([Elwert, 2013, p. 4](zotero://select/library/items/IV5VHEJH))
  
* [Go to annotation](zotero://open-pdf/library/items/BGVHXG7V?page=4&annotation=IRT5DFZJ) “Identification refers to the possibility of correctly estimating a causal effect asymptotically from a given set of observed variables, as the number of observations goes to infinity. Actually estimating, that is, computing, the causal effect from finite sample data is a different matter.” ([Elwert, 2013, p. 4](zotero://select/library/items/IV5VHEJH))
  
* [Go to annotation](zotero://open-pdf/library/items/BGVHXG7V?page=4&annotation=URVLPUGC) “It is often far from obvious how one might specify a parametric statistical model to estimate the parameters of a causal model.” ([Elwert, 2013, p. 4](zotero://select/library/items/IV5VHEJH))

Furthermore, a statistical model is not the same thing as a causal model. We need to keep firm the distinction between causal models and statistical models. As detailed below, the interpretation of a statistical model can change dramatically given different causal models.

Importantly, causal models make no statistical statements about the nature of the causal effect. Causal models simply specify or identify that an effect indeed exists.

* [Go to annotation](zotero://open-pdf/library/items/BGVHXG7V?page=4&annotation=TELAD37A) “Conversely, it is impossible to offer a causal interpretation of a statistical model absent an explicitly stated causal model: The same regression coefficient may yield drastically different interpretations depending on which causal model the analyst believes to be true. The common practice of writing a causal model in regression-like algebraic notation, or, worse, of writing regression equations in lieu of specifying an explicit causal model, can lead to serious confusion.” ([Elwert, 2013, p. 4](zotero://select/library/items/IV5VHEJH))
  
* [Go to annotation](zotero://open-pdf/library/items/BGVHXG7V?page=5&annotation=GAHECKFY) “They make no statement about the distribution of the variables (e.g., normal, Poisson), the functional form of the direct effects (e.g., linear, nonlinear, stepwise), or the magnitude of the causal effects.” ([Elwert, 2013, p. 5](zotero://select/library/items/IV5VHEJH))

### Definitions of DAGs

* DAGs have three elements:
	* Variables (nodes or vertices)
	* Arrows (edges) -> represent direct causal effects.
	* Missing arrows -> represent no direct causal effect.

* Path definition -> If you follow the arrows, it forms a causal path. If you ignore the arrows, you have a non-causal path. This sometimes trips me up. When thinking of paths, the direction does not *always* matter.

	* [Go to annotation](zotero://open-pdf/library/items/BGVHXG7V?page=5&annotation=WA8CYRXW) “Paths are sequences of adjacent arrows that traverse any given variable at most once. The arrows along a path may point in any direction. Causal paths are paths in which all arrows point away from the treatment and toward the outcome; all other paths are called non-causal paths.” ([Elwert, 2013, p. 5](zotero://select/library/items/IV5VHEJH))

* DAGs require a lot of strong assumptions -> you have properly represented all direct causal relationships and you have captured every relevant variable.

	* [Go to annotation](zotero://open-pdf/library/items/BGVHXG7V?page=6&annotation=QM3FGY2E) “When working with DAGs, the analyst (for the most part) needs to assume that the DAG captures the causal structure of everything that matters about a process.” ([Elwert, 2013, p. 6](zotero://select/library/items/IV5VHEJH))
	  
	* [Go to annotation](zotero://open-pdf/library/items/BGVHXG7V?page=6&annotation=B6M3RI6C) “As a conventional shorthand, causal DAGs usually do not display the idiosyncratic factors generically assumed to affect each variable in the DAG, that is, exogenous non-common causes (sometimes called independent error terms)... ” ([Elwert, 2013, p. 6](zotero://select/library/items/IV5VHEJH)) Although Pearl has then in his textbook. It is very important to not forget about the error terms.
	  
* DAGs are acyclic because they have no directed cycles and no loops. Most theoretical and practical applications of DAGs assume true simultaneity does not exist and one needs to more properly specify temporality. Apparently, theory exists for cyclic graphs, though.
  
* DAGs can be interpreted as nonparametric [[Structural equation modeling]]. As a result, DAGs can encode [[moderator]] analysis and [[interaction analysis]].
  
	* Assume A -> B -> C <- D. This DAG would allows the causal effect of B on C to vary with D since the DAG states C causally depends on B and D. You would encode this interaction or moderation effect statistically in the specified structural equations. Effect modification and interactions in DAGs need to be read from the d-separation constraints in the model.

### Three Sources of Association

Chains are causation. Forks are issues of confounding (A does not cause B but rather some common ancestor causes both A and B). Colliders are issues of endogenous selection. Dashed lines between two variables without any arrowheads indicate an endogenous selection.

* [Go to annotation](zotero://open-pdf/library/items/BGVHXG7V?page=6&annotation=E3WNKB5B) “Conveniently, these structures correspond exactly to causation, confounding, and endogenous selection.” ([Elwert, 2013, p. 6](zotero://select/library/items/IV5VHEJH))

### D-separation and Testable Implications

* D-separation is an algorithm which determines, for any given DAG, if two variables will statistically independent given some set (potentially empty) of conditioning variables.

	* Two nodes are separated if every path between them is blocked i.e., if there is a collider that has not been controlled for or a non-collider has been controller for.
  
* If two variables are d-connected, it indicates there is a path between the two variables conditioned on some set of variables Z -> the variables are statistically dependent.
  
* D-separation is a powerful tool because it creates empirical implications (statistical independence and dependence between variables) which can then be verified. While verification will not prove the causal model correct, if some set of variables do not follow the rules set forth by the DAG, that would be evidence that the DAG is incorrectly specified.
  
* Importantly, as mentioned above but worth emphasizing, the independence structure of some observed set of variables can be consistent with multiple, potentially contradictory DAGs. 

	* [Go to annotation](zotero://open-pdf/library/items/BGVHXG7V?page=10&annotation=ZDUY5YNW) “Although the validity of a causal assumption cannot generally be tested against the data in isolation (because that would require ruling out unmeasured confounders, which is itself a causal assumption (Robins and Wasserman 1999), combinations of assumptions can have testable implications (see Chap. 15 by Bollen and Pearl, this volume). One of the important practical uses of d-separation is that it enumerates the testable implications of a causal model. Table 13.1 lists all pairwise marginal and conditional independencies implied by the DAG in Fig. 13.6. The terms involving only observed variables are the empirically testable implications. The terms involving unobserved variables are not empirically testable. To the extent that the testable predictions are not substantiated in the datasubject to the usual serious caveats about type I and type II errors of significance testing—the DAG does not accurately represent the mechanism by which the data were generated.” ([Elwert, 2013, p. 10](zotero://select/library/items/IV5VHEJH))

	* [Go to annotation](zotero://open-pdf/library/items/BGVHXG7V?page=11&annotation=ADS9GJBT) “The correct DAG, however, cannot be inferred from the data alone. Among other possibilities, the correct DAG might include the arrow X -> $Z_2$, or the arrow X <- $Z_2$, or another unmeasured confounder, V, X <- V -> $Z_2$. DAGs have unambiguous implications for the independence structure of compatible probability distributions, but the independence structure of a distribution of observed variables is consistent with multiple DAGs.” ([Elwert, 2013, p. 11](zotero://select/library/items/IV5VHEJH))

### Causal Identification

DAGs are incredibly powerful because they can also specify when (and if) a casual effect can be identified using observational data alone. Specifically, DAGs tell the researcher what specific variables they must condition on (if any) to recover the causal effect. In this way, researchers avoid under-controlling ([[omitted variable bias]]) but also the less appreciated over-controlling or [[collider bias]].

Essentially, the adjustment set for identifying the causal effect must block all non-causal paths without blocking any causal paths.

* There can be many different ways to recover the causal effect i.e., different adjustment sets.

* [Go to annotation](zotero://open-pdf/library/items/BGVHXG7V?page=15&annotation=B4UQCMFB) “The adjustment criterion is theoretically important because it provides a direct link to the potential outcomes framework of causal inference. Conditional ignorability of treatment assignment with respect to the potential outcomes, $Y^T \perp\!\!\!\perp T|Z$; (Rosenbaum and Rubin 1983) implies that the adjustment criterion is met by adjusting for Z; and the fact that the adjustment criterion is met implies conditional ignorability (Shpitser et al. 2010). Knowledge of the DAG therefore helps analysts understand when conditional ignorability is met and when it is not met.” ([Elwert, 2013, p. 15](zotero://select/library/items/IV5VHEJH))

The adjustment criterion implies several narrower identification criteria which offer guidance for quickly finding sufficient adjustment sets. One is the backdoor criterion. The causal effect is identified if you can close all so-called backdoor paths which could feasibly be causing T and then Y. If you are interested in the causal effect of T on Y.

* [Go to annotation](zotero://open-pdf/library/items/BGVHXG7V?page=16&annotation=VET54Y3T) “The analyst therefore only needs to worry about non-causal paths that start with an arrow into treatment, -> T. Such non-causal paths are called backdoor paths. The [[backdoor criterion]] (Pearl 1993, 2009): A set of observed variables Z (which may be empty) satisfies the backdoor criterion relative to the total causal effect of a treatment T on an outcome Y if: 
	1. No element of Z is a descendant of T.
	2. Z blocks all backdoor paths from T to Y.
	3. If Z satisfies the backdoor criterion, then the total causal effect of T on Y is nonparametrically identified” ([Elwert, 2013, p. 16](zotero://select/library/items/IV5VHEJH))

### Beyond adjustment sets

If you cannot identify an adjustment set through the backdoor criterion or other related criterion, there exist still more techniques.

* Alternative #1 -> [[front door criterion]]
	* [Go to annotation](zotero://open-pdf/library/items/BGVHXG7V?page=18&annotation=ES6UR3F5)“ Numerous additional strategies exist that may work even if treatment is not ignorable and no set of covariates satisfies the adjustment criterion. All of these strategies can be represented graphically with DAGs, and all ultimately rely on d-separation. One of the alternatives to the adjustment criterion is Pearl’s (1995) front door identification criterion. Front door identification relies on piecing together a total causal effect from its constituent parts through repeated application of the backdoor criterion.” ([Elwert, 2013, p. 18](zotero://select/library/items/IV5VHEJH))
	  
* Everything is really just a special case of the [[do-calculus]] though. It is an algorithm which can detect the identifiability of all identifiable causal effects.

	* [Go to annotation](zotero://open-pdf/library/items/BGVHXG7V?page=18&annotation=CHBNAVL7) “The most general nonparametric graphical identification criterion is Pearl’s calculus of intervention, or do-calculus (1995, 2009: Section 3.4). Shpitser and Pearl (2006) prove that the do-calculus is complete in that it detects the identifiability of all nonparametrically identifiable causal effects of interventions. All other graphical identification criteria, including the adjustment (ignorability)and front door criteria, are special cases of the do-calculus.” ([Elwert, 2013, p. 18](zotero://select/library/items/IV5VHEJH))

Even if a causal effect is not identifiable by any of the nonparametric criteria, one can still identify a causal effect through parametric assumptions and using something like a [[instrumental variable]].

* [Go to annotation](zotero://open-pdf/library/items/BGVHXG7V?page=18&annotation=PYH5G45W) “If a causal effect is not identifiable by any of the above nonparametric criteria (e.g., if treatment and a child of treatment on a causal pathway are confounded by an unobserved variable), then the analyst may be still be able to achieve identification if he or she can defend additional parametric assumptions. Pearl (2009 : chapter 5) discusses graphical criteria for identification in linear models; Brito and Pearl (2002) give a graphical criterion for detecting instrumental variables...” ([Elwert, 2013, p. 18](zotero://select/library/items/IV5VHEJH))

### Conclusion

You need to specify your causal model, ideally in the form of a DAG. In the statistical models we estimate, we are already assuming a causal model under the surface (given that we are conditioning on some set of variables). Only by making our assumptions explicit can we be sure we are correctly controlling for what should be controlled for.

Even an unrealistically sparse DAG (or an impossibly complicated DAG) can serve an important purpose in highlighting problems in theory or concentrating efforts on where theory should go. Simple DAGs for simpler problems may also help identify wrong (or correct assumptions) in the larger, more realistic and complicated DAGs.

* [Go to annotation](zotero://open-pdf/library/items/BGVHXG7V?page=27&annotation=X4WICAY2) “If the DAG is incorrect, the identification conclusions drawn from it may be incorrect as well. It would be misguided, however, to blame DAGs for what ultimately are limitations of substantive scientific knowledge. The identification of causal effects requires causal assumptions regardless of how these assumptions are notated. DAGs seem to be especially well suited to draw attention to incomplete or implausible causal assumptions. This is a good thing. Assumptions do not disappear simply because they are hidden in a thicket of notation, and they cannot be corrected unless they are noticed and understood (Pearl 2009). One hopes that transparency might spur scientific progress. A related problem is that the common-cause-inclusion requirement of causal DAGs quickly leads to unmanageably large DAGs in non-experimental settings. Taking the shortcut of placing bi-headed arrows on pairs of variables that one suspects of being confounded usually leads to the disappearance of exclusion restrictions and hence to the realization that hardly any causal effect appears identifiable. This too, however, can hardly be blamed on the graphical framework per se, which merely reveals that poor theory (or strong theory coupled with poor data) rarely supports the identification of causal effects in observational studies.” ([Elwert, 2013, p. 27](zotero://select/library/items/IV5VHEJH))