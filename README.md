# Bivariate-Modeling-of-Green-Data-Center-Power-Analysis
Decoupled bivariate simulation framework modeling data center power consumption by treating network traffic (NHPP) and computational workload (Lognormal) as independent signals, revealing energy-proportionality gaps across a 520-VM, 49-blade multi-tenant cluster.The rapid growth of cloud computing, big data, and AI has made data centers vital infrastructure but also heavy electricity consumers (1%–2% globally). Traditional power estimation models often err by assuming a linear,
direct coupling between network traffic and computational workloads, a valid
assumption only for simple, synchronous applications. In contrast, modern
multi-tenant data centers run numerous asynchronous background tasks (e.g.,
machine learning checkpointing, database indexing) that consume power independently of network traffic. To address this, the report presents a novel
decoupled bivariate modeling framework that treats network ingress request
density and internal computational execution amplitude as independent signals. The simulation models a realistic multi-tenant data center pod with
520 virtual machines over 49 physical blades sharing 69 CPU cores. Network
traffic is generated using a Nonhomogeneous Poisson Process modulated by
a 24-hour diurnal pattern, while task processing demands follow a Lognormal distribution, with mathematical isolation enforced per VM to eliminate
coupling. Aggregated over the fleet, stochastic fluctuations smooth out, revealing a clear diurnal traffic wave alongside a flat, stable 7.4% cluster-wide
compute baseline. Combining the two independent tracks via a calibrated
linear power superposition model matching a 49-blade server pod reveals that
although power usage follows user traffic fluctuations, a significant baseline
power draw (6,000 W floor) persists during off-peak hours due to background
compute loads. This highlights a major green scheduling challenge in reducing data center energy consumption.
