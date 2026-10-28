| Decision area | Implementation / decision | Justification | Limitations |
|---|---|---|---|
| Instance type | General-purpose EC2 instance | Balances compute, memory and networking for a standard workload | May not suit specialised compute or memory requirements |
| Testing capacity | Spot Instance | Low-cost option for short-lived test workloads | Can be interrupted when AWS needs the capacity |
| Production capacity | Reserved Instance | Suitable for predictable, steady-state usage where commitment-based discounts are appropriate | Requires a commitment and may be less suitable if usage changes |
| Operating Region | Select a Region close to intended users and external systems | Helps reduce network latency | Location alone does not guarantee lowest cost or best availability |
| Worldwide production | Evaluate Dedicated Hosts or Dedicated Instances if requirements justify them | Provides dedicated tenancy options for specific isolation or licensing requirements | Higher cost; dedicated tenancy does not itself provide worldwide availability |