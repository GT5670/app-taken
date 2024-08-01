# Trusted Application Pipeline Software Template

This application, **app-taken**, was created from a Trusted Application Pipeline Software Template.

The software templates create a new source and gitops deployment repositories with a sample source application. 

## Repositories

Traceback (most recent call last):
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/flask/app.py", line 1498, in __call__
    return self.wsgi_app(environ, start_response)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/flask/app.py", line 1476, in wsgi_app
    response = self.handle_exception(e)
               ^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/flask/app.py", line 1473, in wsgi_app
    response = self.full_dispatch_request()
               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/flask/app.py", line 882, in full_dispatch_request
    rv = self.handle_user_exception(e)
         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/flask/app.py", line 880, in full_dispatch_request
    rv = self.dispatch_request()
         ^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/flask/app.py", line 865, in dispatch_request
    return self.ensure_sync(self.view_functions[rule.endpoint])(**view_args)  # type: ignore[no-any-return]
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/app.py", line 113, in analyze
    summary = summarizer(summary_input, max_length=200, min_length=50, do_sample=False)
              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/transformers/pipelines/text2text_generation.py", line 269, in __call__
    return super().__call__(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/transformers/pipelines/text2text_generation.py", line 167, in __call__
    result = super().__call__(*args, **kwargs)
             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/transformers/pipelines/base.py", line 1254, in __call__
    return self.run_single(inputs, preprocess_params, forward_params, postprocess_params)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/transformers/pipelines/base.py", line 1261, in run_single
    model_outputs = self.forward(model_inputs, **forward_params)
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/transformers/pipelines/base.py", line 1161, in forward
    model_outputs = self._forward(model_inputs, **forward_params)
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/transformers/pipelines/text2text_generation.py", line 191, in _forward
    output_ids = self.model.generate(**model_inputs, **generate_kwargs)
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/torch/utils/_contextlib.py", line 115, in decorate_context
    return func(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/transformers/generation/utils.py", line 1696, in generate
    model_kwargs = self._prepare_encoder_decoder_kwargs_for_generation(
                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/transformers/generation/utils.py", line 539, in _prepare_encoder_decoder_kwargs_for_generation
    model_kwargs["encoder_outputs"]: ModelOutput = encoder(**encoder_kwargs)
                                                   ^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/torch/nn/modules/module.py", line 1532, in _wrapped_call_impl
    return self._call_impl(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/torch/nn/modules/module.py", line 1541, in _call_impl
    return forward_call(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/transformers/models/bart/modeling_bart.py", line 1168, in forward
    embed_pos = self.embed_positions(input)
                ^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/torch/nn/modules/module.py", line 1532, in _wrapped_call_impl
    return self._call_impl(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/torch/nn/modules/module.py", line 1541, in _call_impl
    return forward_call(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/transformers/models/bart/modeling_bart.py", line 130, in forward
    return super().forward(positions + self.offset)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/torch/nn/modules/sparse.py", line 163, in forward
    return F.embedding(
           ^^^^^^^^^^^^
  File "/home/gtrivedi/Desktop/demo/demo_env/lib64/python3.12/site-packages/torch/nn/functional.py", line 2264, in embedding
    return torch.embedding(weight, input, padding_idx, scale_grad_by_freq, sparse)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
IndexError: index out of range in self
