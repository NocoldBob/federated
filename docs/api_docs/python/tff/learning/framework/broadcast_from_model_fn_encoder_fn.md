<div itemscope itemtype="http://developers.google.com/ReferenceObject">
<meta itemprop="name" content="tff.learning.framework.broadcast_from_model_fn_encoder_fn" />
<meta itemprop="path" content="Stable" />
</div>

# tff.learning.framework.broadcast_from_model_fn_encoder_fn

Builds `StatefulBroadcastFn` for weights of model returned by `model_fn`.

```python
tff.learning.framework.broadcast_from_model_fn_encoder_fn(
    model_fn,
    encoder_fn
)
```

<a target="_blank" href=http://github.com/tensorflow/federated/tree/master/tensorflow_federated/python/learning/framework/encoding_utils.py>View
source</a>

<!-- Placeholder for "Used in" -->

#### This

Args:

*   <b>`model_fn`</b>: A Python callable with no arguments function that returns
    a
    <a href="../../../tff/learning/Model.md"><code>tff.learning.Model</code></a>.
*   <b>`encoder_fn`</b>: A Python callable with a single argument, which is
    expected to be a `tf.Tensor` of shape and dtype to be encoded.

#### Returns:

A `StatefulBroadcastFn` for encoding and broadcasting the weights of model
created by `model_fn`.

#### Raises:

*   <b>`TypeError`</b>: If `model_fn` or `encoder_fn` are not callable objects.
