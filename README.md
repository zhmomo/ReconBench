# ReconBench
The full dataset can be found on https://huggingface.co/datasets/zhmzhmzhm/ReconBench.
The structure of each line is 
```json
{
  "trace_id": str
  "old_trace_id": str
  "num_nodes": int
  "num_of_egress": int(number of egress nodes)
  "egress_node": list(all egress nodes)
  "other_nodes": list(all other nodes)
  "before_next_hops": dict(key means node, value means next hop, before reconfiguration)
  "after_next_hops": dict(key means node, value means next hop, after reconfiguration)
  "reconfig_changes": list[str1,str2,str3](the order of reconfiguration change, each item in it means node str1's next hop change for str2 to str3)
  "prompt_text": str(prompt)
  "ground_truth": bool|str|list(groundtruth)
  "cot": str(cot of solving)
}
```
