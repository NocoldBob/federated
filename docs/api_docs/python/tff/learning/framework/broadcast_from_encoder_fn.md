<div itemscope itemtype="http://developers.google.com/ReferenceObject">
<meta itemprop="name" content="tff.learning.framework.broadcast_from_encoder_fn" />
<meta itemprop="path" content="Stable" />
</div>

# tff.learning.framework.broadcast_from_encoder_fn

Builds `StatefulBroadcastFn` for `values`.

```python
tff.learning.framework.broadcast_from_encoder_fn(
    values,
    encoder_fn
)
```

<a target="_blank" href=http://github.com/tensorflow/federated/tree/master/tensorflow_federated/python/learning/framework/encoding_utils.py>View
source</a>

<!-- Placeholder for "Used in" -->

This method creates a `SimpleEncoder` for every value in `values`, as returned
by `encoder_fn`.

#### Args:

*   <b>`values`</b>: A possible nested structure of values to be broadcasted.
*   <b>`encoder_fn`</b>: A Python callable with a single argument, which is
    expected to be a `tf.Tensor` of shape and dtype to be encoded.

#### Returns:

A `StatefulBroadcastFn` for encoding and broadcasting `values`.

#### Raises:

*   <b>`TypeError`</b>: If `encoder_fn` is not a callable object.
