# llama-cpp-python-wheels

Prebuilt [llama-cpp-python](https://github.com/abetlen/llama-cpp-python) wheels with GPU
acceleration, published as GitHub Releases.

| Platform | Backend | Wheel tag |
|---|---|---|
| macOS 11+ on Apple Silicon | Metal | `macosx_11_0_arm64` |
| Windows x64 | Vulkan | `win_amd64` |

## How they are built

- Each release is built from the unmodified llama-cpp-python source distribution on PyPI
  of the version in the release name (`llama-cpp-python-v<version>`).
- The wheels are built and uploaded by SkyReve's CI. There is no source code in this
  repository.
- A release is never rebuilt or replaced once it is published, so a wheel's hash stays
  valid for as long as the release exists.

## Using a wheel

Download the wheel for your platform from
[Releases](https://github.com/SkyReve/llama-cpp-python-wheels/releases) and install it,
or point your package manager at its URL. Pin the wheel's SHA-256 hash when you do.

The Vulkan wheel needs a GPU driver that provides Vulkan (`vulkan-1.dll`); recent NVIDIA,
AMD, and Intel drivers do.

## Support

These wheels are built for SkyReve's own products and published as-is. Issues and pull
requests are not monitored. For problems with llama-cpp-python itself, use the
[upstream project](https://github.com/abetlen/llama-cpp-python/issues).

## License

The wheels contain llama-cpp-python and llama.cpp, both under the MIT License. Their
license texts are included in each wheel's `.dist-info` directory. The files in this
repository are under the MIT License; see [LICENSE](LICENSE).
