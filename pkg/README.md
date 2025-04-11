# infini-gram

To use this package, please check out its **documentation** here: <https://infini-gram.io/pkg_doc>

To learn more about infini-gram:
* Paper: <https://arxiv.org/abs/2401.17377>
* Project Home: <https://infini-gram.io>
* Web Interface: <https://infini-gram.io/demo>
* API Endpoint: <https://infini-gram.io/api_doc>
* Python Package: <https://pypi.org/project/infini-gram>
* Code: <https://github.com/liujch1998/infini-gram>

## Building Custom Index

```bash
cd pkg

# Install Rust
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source "$HOME/.cargo/env"

# Go to `pkg/` and compile the Rust indexing code, and move the executable to the correct place:
cargo build --release
mv target/release/rust_indexing infini_gram/

# Install the python `infini_gram` package
pip install -e .

# Run the indexing script
python -m infini_gram.indexing --data_dir ... --save_dir ...
```

## Citation

If you find infini-gram useful, please kindly cite our paper:
```bibtex
@article{Liu2024InfiniGram,
  title={Infini-gram: Scaling Unbounded n-gram Language Models to a Trillion Tokens},
  author={Liu, Jiacheng and Min, Sewon and Zettlemoyer, Luke and Choi, Yejin and Hajishirzi, Hannaneh},
  journal={arXiv preprint arXiv:2401.17377},
  year={2024}
}
```
