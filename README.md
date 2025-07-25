<div align="center">

# ComfyUI
**The most powerful and modular visual AI engine and application.**

[![Website][website-shield]][website-url]
[![Dynamic JSON Badge][discord-shield]][discord-url]
[![Twitter][twitter-shield]][twitter-url]
[![Matrix][matrix-shield]][matrix-url]
<br>
[![][github-release-shield]][github-release-link]
[![][github-release-date-shield]][github-release-link]
[![][github-downloads-shield]][github-downloads-link]
[![][github-downloads-latest-shield]][github-downloads-link]
<img width="1634" height="964" alt="image" src="https://github.com/user-attachments/assets/e6656084-6e2d-4c15-8b42-01ea30ec0202" />



[matrix-shield]: https://img.shields.io/badge/Matrix-000000?style=flat&logo=matrix&logoColor=white
[matrix-url]: https://app.element.io/#/room/%23comfyui_space%3Amatrix.org
[website-shield]: https://img.shields.io/badge/ComfyOrg-4285F4?style=flat
[website-url]: https://www.comfy.org/
<!-- Workaround to display total user from https://github.com/badges/shields/issues/4500#issuecomment-2060079995 -->
[discord-shield]: https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fdiscord.com%2Fapi%2Finvites%2Fcomfyorg%3Fwith_counts%3Dtrue&query=%24.approximate_member_count&logo=discord&logoColor=white&label=Discord&color=green&suffix=%20total
[discord-url]: https://www.comfy.org/discord
[twitter-shield]: https://img.shields.io/twitter/follow/ComfyUI
[twitter-url]: https://x.com/ComfyUI

[github-release-shield]: https://img.shields.io/github/v/release/comfyanonymous/ComfyUI?style=flat&sort=semver
[github-release-link]: https://github.com/comfyanonymous/ComfyUI/releases
[github-release-date-shield]: https://img.shields.io/github/release-date/comfyanonymous/ComfyUI?style=flat
[github-downloads-shield]: https://img.shields.io/github/downloads/comfyanonymous/ComfyUI/total?style=flat
[github-downloads-latest-shield]: https://img.shields.io/github/downloads/comfyanonymous/ComfyUI/latest/total?style=flat&label=downloads%40latest
[github-downloads-link]: https://github.com/comfyanonymous/ComfyUI/releases

ComfyUI lets you design and execute advanced stable diffusion pipelines using a graph/nodes/flowchart based interface. Available on Windows, Linux, and macOS.

## Get Started

#### [Desktop Application](https://www.comfy.org/download)
- The easiest way to get started
- Available on Windows & macOS

#### [Windows Portable Package](#installing)
- Get the latest commits and completely portable
- Available on Windows

#### [Manual Install](#manual-install-windows-linux)
Supports all operating systems and GPU types (NVIDIA, AMD, Intel, Apple Silicon, Ascend)

## [Examples](https://comfyanonymous.github.io/ComfyUI_examples/)
See what ComfyUI can do with the [example workflows](https://comfyanonymous.github.io/ComfyUI_examples/).

## Features
- Nodes/graph/flowchart interface to experiment and create complex Stable Diffusion workflows without needing to code anything
- Supports:
  - SD1.x, SD2.x
  - [SDXL](https://comfyanonymous.github.io/ComfyUI_examples/sdxl/)
  - [SDXL Turbo](https://comfyanonymous.github.io/ComfyUI_examples/sdturbo/)
  - [Stable Cascade](https://comfyanonymous.github.io/ComfyUI_examples/stable_cascade/)
  - [SD3](https://comfyanonymous.github.io/ComfyUI_examples/sd3/)
- Asynchronous Queue system
- Many optimizations: Only re-executes the parts of the workflow that changes between executions
- Works even if you don't have a GPU with: ```--cpu``` (slow)
- Can load ckpt, safetensors and diffusers models/checkpoints. Standalone VAEs and CLIP models
- Embeddings/Textual inversion
- [Loras (regular, locon and loha)](https://comfyanonymous.github.io/ComfyUI_examples/lora/)
- [Hypernetworks](https://comfyanonymous.github.io/ComfyUI_examples/hypernetworks/)
- Loading full workflows (with seeds) from generated PNG files
- Saving/Loading workflows as Json files
- Nodes interface can be used to create complex workflows like one for [Hires fix](https://comfyanonymous.github.io/ComfyUI_examples/2_pass_txt2img/) or much more advanced ones
- [Area Composition](https://comfyanonymous.github.io/ComfyUI_examples/area_composition/)
- [Inpainting](https://comfyanonymous.github.io/ComfyUI_examples/inpaint/) with both regular and inpainting models
- [ControlNet and T2I-Adapter](https://comfyanonymous.github.io/ComfyUI_examples/controlnet/)
- [Upscale Models (ESRGAN, ESRGAN variants, SwinIR, Swin2SR, etc...)](https://comfyanonymous.github.io/ComfyUI_examples/upscale_models/)
- [unCLIP Models](https://comfyanonymous.github.io/ComfyUI_examples/unclip/)
- [GLIGEN](https://comfyanonymous.github.io/ComfyUI_examples/gligen/)
- [Model Merging](https://comfyanonymous.github.io/ComfyUI_examples/model_merging/)
- Latent previews with [TAESD](#how-to-show-high-quality-previews)
- Works fully offline: core will never download anything unless you want to

Workflow examples can be found on the [Examples page](https://comfyanonymous.github.io/ComfyUI_examples/)

## Shortcuts

| Keybind                            | Explanation                                                                                                        |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| `Ctrl` + `Enter`                   | Queue up current graph for generation                                                                              |
| `Ctrl` + `Shift` + `Enter`         | Queue up current graph as first for generation                                                                     |
| `Ctrl` + `Alt` + `Enter`           | Cancel current generation                                                                                          |
| `Ctrl` + `Z`/`Ctrl` + `Y`          | Undo/Redo                                                                                                          |
| `Ctrl` + `S`                       | Save workflow                                                                                                      |
| `Ctrl` + `O`                       | Load workflow                                                                                                      |
| `Ctrl` + `A`                       | Select all nodes                                                                                                   |
| `Alt` + `C`                        | Collapse/uncollapse selected nodes                                                                                 |
| `Ctrl` + `M`                       | Mute/unmute selected nodes                                                                                         |
| `Ctrl` + `B`                       | Bypass selected nodes (acts like the node was removed from the graph and the wires reconnected through)            |
| `Delete`/`Backspace`               | Delete selected nodes                                                                                              |
| `Ctrl` + `Backspace`               | Delete the current graph                                                                                           |
| `Space`                            | Move the canvas around when held and moving the cursor                                                             |
| `Ctrl`/`Shift` + `Click`           | Add clicked node to selection                                                                                      |
| `Ctrl` + `C`/`Ctrl` + `V`          | Copy and paste selected nodes (without maintaining connections to outputs of unselected nodes)                     |
| `Ctrl` + `C`/`Ctrl` + `Shift` + `V`| Copy and paste selected nodes (maintaining connections from outputs of unselected nodes to inputs of pasted nodes) |
| `Shift` + `Drag`                   | Move multiple selected nodes at the same time                                                                      |
| `Ctrl` + `D`                       | Load default graph                                                                                                 |
| `Alt` + `+`                        | Canvas Zoom in                                                                                                     |
| `Alt` + `-`                        | Canvas Zoom out                                                                                                    |
| `Ctrl` + `Shift` + LMB + Vertical drag | Canvas Zoom in/out                                                                                          |
| `P`                                | Pin/Unpin selected nodes                                                                                           |
| `Ctrl` + `G`                       | Group selected nodes                                                                                               |
| `Q`                                | Toggle visibility of the queue                                                                                     |
| `H`                                | Toggle visibility of history                                                                                       |
| `R`                                | Refresh graph                                                                                                      |
| `F`                                | Show/Hide menu                                                                                                     |
| `.`                                | Fit view to selection (Whole graph when nothing is selected)                                                       |
| Double-Click LMB                   | Open node quick search palette                                                                                     |
| `Shift` + Drag                     | Move multiple wires at once                                                                                        |
| `Ctrl` + `Alt` + LMB               | Disconnect all wires from clicked slot                                                                             |

`Ctrl` can also be replaced with `Cmd` instead for macOS users

# Installing

## Windows Portable

There is a portable standalone build for Windows that should work for running on Nvidia GPUs or for running on your CPU only on the [releases page](https://github.com/comfyanonymous/ComfyUI/releases).

### [Direct link to download](https://github.com/comfyanonymous/ComfyUI/releases/latest/download/ComfyUI_windows_portable_nvidia.7z)

Simply download, extract with [7-Zip](https://7-zip.org) and run. Make sure you put your Stable Diffusion checkpoints/models (the huge ckpt/safetensors files) in: `ComfyUI\models\checkpoints`

If you have trouble extracting it, right click the file -> properties -> unblock

#### How do I share models between another UI and ComfyUI?

See the [Config file](extra_model_paths.yaml.example) to set the search paths for models. In the standalone windows build you can find this file in the ComfyUI directory. Rename this file to `extra_model_paths.yaml` and edit it with your favorite text editor.

## Manual Install (Windows, Linux)

Git clone this repo.

Put your SD checkpoints (the huge ckpt/safetensors files) in: `models/checkpoints`

Put your VAE in: `models/vae`

### NVIDIA

Nvidia users should install pytorch with this command:

```pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121```

#### Troubleshooting

If you get the "Torch not compiled with CUDA enabled" error, uninstall torch with:

```pip uninstall torch```

And install it again with the command above.

### AMD GPUs (Linux only)

AMD users can install rocm and pytorch with pip if you don't have it already installed, this is the command to install pytorch with rocm:

```pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/rocm5.6```

### Intel GPUs

Intel Arc GPU users can install pytorch with:

```pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/xpu```

### Dependencies

Install the dependencies by opening your terminal inside the ComfyUI folder and:

```pip install -r requirements.txt```

After this you should have everything installed and can proceed to running ComfyUI.

### Others:

#### Apple Mac silicon

You can install ComfyUI in Apple Mac silicon (M1 or M2) with any recent macOS version.

1. Install pytorch nightly. For instructions, read the [Accelerated PyTorch training on Mac](https://developer.apple.com/metal/pytorch/) Apple Developer guide (make sure to install the latest pytorch nightly).
1. Follow the [ComfyUI manual installation](#manual-install-windows-linux) instructions for Windows and Linux.
1. Install the ComfyUI [dependencies](#dependencies). If you have another Stable Diffusion UI [you might be able to reuse the dependencies](#i-already-have-another-ui-for-stable-diffusion-installed-do-i-really-have-to-install-all-of-these-dependencies).
1. Launch ComfyUI by running `python main.py`

> **Note**: Remember to add your models, VAE, LoRAs etc. to the corresponding Comfy folders, as discussed in [ComfyUI manual installation](#manual-install-windows-linux).

#### DirectML (AMD Cards on Windows)

This is very badly supported and is not recommended. There are some unofficial builds of pytorch ROCm on windows that exist that will give you a much better experience than this. This readme will be updated once official pytorch ROCm builds for windows come out.

```pip install torch-directml``` Then you can launch ComfyUI with: ```python main.py --directml```

# Running

```python main.py```

### For AMD cards not officially supported by ROCm

Try running it with this command if you have issues:

For 6700, 6600 and maybe other RDNA2 or older: ```HSA_OVERRIDE_GFX_VERSION=10.3.0 python main.py```

For AMD 7600 and maybe other RDNA3 cards: ```HSA_OVERRIDE_GFX_VERSION=11.0.0 python main.py```

# Notes

Only parts of the graph that have an output with all the correct inputs will be executed.

Only parts of the graph that change from each execution to the next will be executed, if you submit the same graph twice only the first will be executed. If you change the last part of the graph only the part you changed and the part that depends on it will be executed.

Dragging a generated png on the webpage or loading one will give you the full workflow including seeds that were used to create it.

You can use () to change emphasis of a word or phrase like: (good code:1.2) or (bad code:0.8). The default emphasis for () is 1.1. To use () characters in your actual prompt escape them like \\( or \\).

You can use {day|night}, for wildcard/dynamic prompts. With this syntax "{wild|card|test}" will be randomly replaced by either "wild", "card" or "test" by the frontend every time you queue the prompt. To use {} characters in your actual prompt escape them like: \\{ or \\}.

To use a textual inversion concepts/embeddings in a text prompt put them in the models/embeddings directory and use them in the CLIPTextEncode node like this (you can omit the .pt extension):

```embedding:embedding_filename.pt```

## How to show high-quality previews?

The default installation includes a fast latent preview method that's low-resolution. To enable higher-quality previews with [TAESD](https://github.com/madebyollin/taesd), download the [taesd_decoder.pth](https://github.com/madebyollin/taesd/) and place it in the `models/vae_approx` folder. Once it's installed, restart ComfyUI and launch it with `--preview-method taesd` to enable high-quality previews.

## Support and dev channel

[Discord](https://comfy.org/discord): Try the #help or #feedback channels.

[Matrix space: #comfyui_space:matrix.org](https://app.element.io/#/room/%23comfyui_space%3Amatrix.org) (it's like discord but open source).

See also: [https://www.comfy.org/](https://www.comfy.org/)

# QA

### I already have another UI for stable diffusion installed, do I really have to install all of these dependencies?

If your other UI installed pytorch with CUDA then no, you just need the requirements.txt dependencies. Make sure ComfyUI is installed in a separate folder though.

### Which GPU should I buy for this?

For best performance you probably want an Nvidia GPU with as much VRAM as you can get. Having more VRAM will allow you to run larger models and higher resolution images without having to use the `--lowvram` or `--medvram` optimizations.
