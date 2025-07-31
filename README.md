# ReconBench
The full dataset can be found on https://huggingface.co/datasets/zhmzhmzhm/ReconBench.

ReconBench: Benchmarking Large Language Models for Network Reconfiguration with Linear Temporal Logic Constraints

To assemble the ReconBench, we collected a wide spectrum of topologies: realworld networks drawn from production environments ensure relevance, whereas canonical synthetic topologies allow controlled variation of parameters and their measured impact on model performance. We further conducted a systematic set of ablation experiments that vary network size and constraint length.

We release a theoretically grounded and practically relevant dataset—ReconBench and evaluation protocol that comprehensively assesses LLMs’ LTL reasoning under varying parameter regimes. ReconBench combines real and synthetic topologies, derives atomic constraints from network requirements, and generates LTL formulas with a prescribed number of such atoms, yielding ready-to-use training and test splits.

The structure of each line is 
```json
{
  "trace_id": "str",
  "old_trace_id": "str",
  "num_nodes": "int",
  "num_of_egress": "int(number of egress nodes)",
  "egress_node": "list(all egress nodes)",
  "other_nodes": "list(all other nodes)",
  "before_next_hops": "dict(key means node, value means next hop, before reconfiguration)",
  "after_next_hops": "dict(key means node, value means next hop, after reconfiguration)",
  "reconfig_changes": "list[str1,str2,str3](the order of reconfiguration change, each item in it means node str1's next hop change for str2 to str3)",
  "prompt_text": "str(prompt)",
  "ground_truth": "bool|str|list(groundtruth)",
  "cot": "str(cot of solving)",
}
```
