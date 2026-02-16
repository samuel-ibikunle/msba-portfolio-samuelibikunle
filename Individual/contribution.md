Personally contributed most
Built a solid churn/retention modeling workflow: I set up a repeatable tuning + evaluation approach (RF + CV), checked class imbalance , and used profiling output to understand the dataset and what might be driving churn.

Focused the project on business-relevant performance, not just  good-looking accuracy. I kept circling back to what metric actually matters for churn prediction and how imbalance affects evaluation.

One decision/approach you advocated for + why
Advocated for tuning around the right objective (AUC/F1/recall) and adding class-weight as a tunable parameter when running random forrest, rather than assuming default accuracy would tell the truth.
Why- Bacauese with a 73/27 split, accuracy can look high even if the model misses churners. So, optimizing the right metric and testing class_weight options is the quickest way to make the model useful for retention actions.

1–2 lessons learned + what you’d improve with more time
Better depends on the metric—changing scoring changes what best means.
Improvements - lock down a single primary metric tied to your retention goal, then report the same metric consistently across experiments and pick a decision threshold intentionally.

Parameter choices are only meaningful if your evaluation is consistent (same scoring, same preprocessing, same split strategy).
Improvements: standardize an experiment template (fixed scoring + same CV + same reporting) so every run is comparable. 

