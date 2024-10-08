# Settings
* Working after change a few lines of codes
* Env worked: nanogpt, of Py 3.10 and transforms 2
* conda_env_nanogpt.yml saved
<pre>
conda install transformers[torch]=2
conda install pytorch==2.4.0 torchvision==0.19.0 torchaudio==2.4.0  pytorch-cuda=11.8 -c pytorch -c nvidia
conda install conda-forge::tiktoken
conda install conda-forge::datasets
</pre>
<pre>
Still errors when using the "python data/openwebtext/prepare.py"

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "C:\Users\flin\git\nanoGPT\data\openwebtext\prepare.py", line 23, in <module>
    dataset = load_dataset("openwebtext", num_proc=num_proc_load_dataset, trust_remote_code=True)
  File "C:\Users\flin\.conda\envs\nanogpt\lib\site-packages\datasets\load.py", line 2096, in load_dataset
    builder_instance.download_and_prepare(
  File "C:\Users\flin\.conda\envs\nanogpt\lib\site-packages\datasets\builder.py", line 924, in download_and_prepare
    self._download_and_prepare(
  File "C:\Users\flin\.conda\envs\nanogpt\lib\site-packages\datasets\builder.py", line 1647, in _download_and_prepare
    super()._download_and_prepare(
  File "C:\Users\flin\.conda\envs\nanogpt\lib\site-packages\datasets\builder.py", line 977, in _download_and_prepare
    split_generators = self._split_generators(dl_manager, **split_generators_kwargs)
  File "Z:\cache_huggingface\modules\datasets_modules\datasets\openwebtext\6f68e85c16ccc770c0dd489f4008852ea9633604995addd0cd76e293aed9e521\openwebtext.py", line 59, in _split_generators
    archives = dl_manager.download(_DATA_FILES)
  File "C:\Users\flin\.conda\envs\nanogpt\lib\site-packages\datasets\download\download_manager.py", line 159, in download
    downloaded_path_or_paths = map_nested(
  File "C:\Users\flin\.conda\envs\nanogpt\lib\site-packages\datasets\utils\py_utils.py", line 528, in map_nested
    mapped = parallel_map(
  File "C:\Users\flin\.conda\envs\nanogpt\lib\site-packages\datasets\utils\experimental.py", line 41, in _inner_fn
    return fn(*args, **kwargs)
  File "C:\Users\flin\.conda\envs\nanogpt\lib\site-packages\datasets\parallel\parallel.py", line 34, in parallel_map
    return _map_with_multiprocessing_pool(
  File "C:\Users\flin\.conda\envs\nanogpt\lib\site-packages\datasets\parallel\parallel.py", line 69, in _map_with_multiprocessing_pool
    mapped = pool.map(single_map_nested_func, split_kwds)
  File "C:\Users\flin\.conda\envs\nanogpt\lib\multiprocessing\pool.py", line 367, in map
    return self._map_async(func, iterable, mapstar, chunksize).get()
  File "C:\Users\flin\.conda\envs\nanogpt\lib\multiprocessing\pool.py", line 774, in get
    raise self._value
FileNotFoundError: An error happened while trying to locate the file on the Hub and we cannot find the requested files in the local cache. Please check your connection and try again or make sure your Internet connection is on.


</pre>