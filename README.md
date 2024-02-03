# Very Simple MoE

This notebook contains a very simple implementation of a Mixture-of-Experts Transformer.

It is closest to a [Switch Transformer](https://arxiv.org/abs/2101.03961), in the following respects:
- It routes each token to one expert
- It uses the same loss to balance experts
- It shrinks the parameters with which each expert is initialized, per that paper's advice

It also differs from it in important ways:
- Switch Transformer, obviously, works on multiple GPUs -- this does not
- This simple does causal language modeling, while Switch Transformer had a masked language modeling target
- Probably tons of stuff that I missed

The point is that it should be a simple-enough MoE implementation that you can just upload some data, train off it, and get lower loss using a MoE than with a Dense Transformer.

A place to start learning, at least.
