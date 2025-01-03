# LV-LLMs
A survey on MM-LLMs for long video understanding. 

Related materials on [From Seconds to Hours: Reviewing MultiModal Large Language Models on Comprehensive Long Video Understanding](https://arxiv.org/pdf/2409.18938)


## Long video understanding MM-LLMs

<table>
  <thead>
    <tr>
      <th>Model</th>
      <th>Year</th>
      <th colspan="2" style="text-align:center;">Backbone</th>
      <th colspan="3" style="text-align:center;">Connector</th>
      <th>Frame</th>
      <th>Token</th>
      <th colspan="3" style="text-align:center;">Training</th>
      <th>Long</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Model</td>
      <td></td>
      <td>Visual Encoder</td>
      <td>LLMs</td>
      <td>Image-level</td>
      <td>Video-level</td>
      <td>Long-video-level</td>
      <td></td>
      <td></td>
      <td>Hardware</td>
      <td>PreT</td>
      <td>IT</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2305.06500">InstructBLIP</a></td>
      <td>23.05</td>
      <td>EVA-CLIP-ViT-G/14</td>
      <td>FlanT5, Vicuna-7B/13B</td>
      <td>Q-Former</td>
      <td>--</td>
      <td>--</td>
      <td>4</td>
      <td>32/128</td>
      <td>16 A100-40G</td>
      <td>Y-N-N</td>
      <td>Y-N-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2305.06355">VideoChat</a></td>
      <td>23.05</td>
      <td>EVA-CLIP-ViT-G/14</td>
      <td>StableVicuna-13B</td>
      <td>Q-Former</td>
      <td>Global multi-head relation aggregator</td>
      <td>--</td>
      <td>8</td>
      <td>/32</td>
      <td>1 A10</td>
      <td>Y-Y-N</td>
      <td>Y-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2306.02858">Video-LLaMA</a></td>
      <td>23.06</td>
      <td>EVA-CLIP-ViT-G/14</td>
      <td>LLaMA, Vicuna</td>
      <td>Q-Former</td>
      <td>Q-Former</td>
      <td>--</td>
      <td>8</td>
      <td>/32</td>
      <td>-</td>
      <td>Y-Y-N</td>
      <td>Y-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2306.05424">Video-ChatGPT</a></td>
      <td>23.06</td>
      <td>CLIP-ViT-L/14</td>
      <td>Vicuna1.1-7B</td>
      <td>Spatial-pooling</td>
      <td>Temporal-pooling</td>
      <td>--</td>
      <td>100</td>
      <td>/356</td>
      <td>8 A100-40G</td>
      <td>N-N-N</td>
      <td>N-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2306.07207">Valley</a></td>
      <td>23.06</td>
      <td>CLIP-ViT-L/14</td>
      <td>StableVicuna-7B/13B</td>
      <td>--</td>
      <td>Transformer and Mean pooling</td>
      <td>--</td>
      <td>0.5 fps</td>
      <td>/256+T</td>
      <td>8 A100 80G</td>
      <td>Y-Y-N</td>
      <td>Y-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="http://openaccess.thecvf.com/content/CVPR2024/papers/Song_MovieChat_From_Dense_Token_to_Sparse_Memory_for_Long_Video_CVPR_2024_paper.pdf">MovieChat</a></td>
      <td>23.07</td>
      <td>EVA-CLIP-ViT-G/14</td>
      <td>LLama-7B</td>
      <td>Q-Former</td>
      <td>Frame merging, Q-Former</td>
      <td>Merging adjacent frames</td>
      <td>2048</td>
      <td>32/32</td>
      <td>-</td>
      <td>E2E</td>
      <td>E2E</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2308.12966">Qwen-VL</a></td>
      <td>23.08</td>
      <td>Openclip-ViT-bigG</td>
      <td>Qwen-7B</td>
      <td>Cross-attention</td>
      <td>--</td>
      <td>--</td>
      <td>4</td>
      <td>/256</td>
      <td>-</td>
      <td>Y-N-N</td>
      <td>Y-N-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://openaccess.thecvf.com/content/CVPR2024/papers/Jin_Chat-UniVi_Unified_Visual_Representation_Empowers_Large_Language_Models_with_Image_CVPR_2024_paper.pdf">Chat-UniVi</a></td>
      <td>23.11</td>
      <td>CLIP-ViT-L/14</td>
      <td>Vicuna1.5-7B</td>
      <td>Token merging</td>
      <td>--</td>
      <td>--</td>
      <td>64</td>
      <td>/112</td>
      <td>-</td>
      <td>Y-N-N</td>
      <td>Y-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2311.10122">Video-LLaVA</a></td>
      <td>23.11</td>
      <td>LanguageBind-ViT-L/14</td>
      <td>Vicuna1.5-7B</td>
      <td>--</td>
      <td>--</td>
      <td>--</td>
      <td>8</td>
      <td>256/2048</td>
      <td>4 A100-80G</td>
      <td>Y-Y-N</td>
      <td>Y-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2311.17043">LLaMA-VID</a></td>
      <td>23.11</td>
      <td>CLIP-ViT-L/14</td>
      <td>Vicuna-7B/13B</td>
      <td colspan="3" style="text-align:center;">Context attention and pooling</td>
      <td>1 fps</td>
      <td>2/</td>
      <td>8 A100</td>
      <td>Y-Y-N</td>
      <td>Y-Y-Y</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td><a href="https://openaccess.thecvf.com/content/CVPR2024/papers/Huang_VTimeLLM_Empower_LLM_to_Grasp_Video_Moments_CVPR_2024_paper.pdf">VTimeLLM</a></td>
      <td>23.11</td>
      <td>CLIP-ViT-L/14</td>
      <td>Vicuna1.5-7B/13B</td>
      <td>Frame feature</td>
      <td>--</td>
      <td>--</td>
      <td>100</td>
      <td>1/100</td>
      <td>1 RTX-4090</td>
      <td>Y-Y-N</td>
      <td>N-Y-N</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td><a href="https://openaccess.thecvf.com/content/CVPR2024/papers/Li_MVBench_A_Comprehensive_Multi-modal_Video_Understanding_Benchmark_CVPR_2024_paper.pdf">VideoChat2</a></td>
      <td>23.11</td>
      <td>EVA-CLIP-ViT-G/14</td>
      <td>Vicuna0-7B</td>
      <td>--</td>
      <td>Q-Former</td>
      <td>--</td>
      <td>16</td>
      <td>/96</td>
      <td>-</td>
      <td>Y-Y-N</td>
      <td>Y-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2312.08870">Vista-LLaMA</a></td>
      <td>23.12</td>
      <td>EVA-CLIP-ViT-G/14</td>
      <td>LLaVa-Vicuna-7B</td>
      <td>Q-Former</td>
      <td>Temporal Q-Former</td>
      <td>--</td>
      <td>16</td>
      <td>32/512</td>
      <td>8 A100-80GB</td>
      <td>E2E</td>
      <td>E2E</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://openaccess.thecvf.com/content/CVPR2024/papers/Ren_TimeChat_A_Time-sensitive_Multimodal_Large_Language_Model_for_Long_Video_CVPR_2024_paper.pdf">TimeChat</a></td>
      <td>23.12</td>
      <td>EVA-CLIP-ViT-G/14</td>
      <td>LLaMA2-7B</td>
      <td>Q-Former</td>
      <td>Sliding window Q-Former</td>
      <td>Time-aware encoding</td>
      <td>96</td>
      <td>/96</td>
      <td>8 V100-32G</td>
      <td>Y-Y-N</td>
      <td>N-N-Y</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2312.02310">VaQuitA</a></td>
      <td>23.12</td>
      <td>CLIP-ViT-L/14</td>
      <td>LLaVA1.5-LLaMA-7B</td>
      <td>--</td>
      <td>Video Perceiver, VQ-Former</td>
      <td>--</td>
      <td>100</td>
      <td>/356</td>
      <td>8 A100-80GB</td>
      <td>E2E</td>
      <td>E2E</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2312.00438">Dolphins</a></td>
      <td>23.12</td>
      <td>CLIP-ViT-L/14</td>
      <td>OpenFlamingo</td>
      <td colspan="2" style="text-align:center;">Perceiver Resamplar, Gated cross-attention</td>
      <td>Time embedding</td>
      <td>--</td>
      <td>--</td>
      <td>4 A100</td>
      <td>N-Y-N</td>
      <td>Y-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2402.11435">Momentor</a></td>
      <td>24.02</td>
      <td>CLIP-ViT-L/14</td>
      <td>LLaMA-7B</td>
      <td colspan="3" style="text-align:center;">Frame feature, Temporal Perception Module, Grounded Event-Sequence Modeling</td>
      <td>300</td>
      <td>1/300</td>
      <td>8 A100</td>
      <td>Y-Y-N</td>
      <td>N-Y-N</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2403.01422">MovieLLM</a></td>
      <td>24.03</td>
      <td>CLIP-ViT-L/14</td>
      <td>Vicuna-7B/13B</td>
      <td colspan="3" style="text-align:center;">Context attention and pooling</td>
      <td>1 fps</td>
      <td>2/</td>
      <td>4 A100</td>
      <td>Y-Y-N</td>
      <td>Y-Y-Y</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td><a href="https://openaccess.thecvf.com/content/CVPR2024/papers/He_MA-LMM_Memory-Augmented_Large_Multimodal_Model_for_Long-Term_Video_Understanding_CVPR_2024_paper.pdf">MA-LMM</a></td>
      <td>24.04</td>
      <td>EVA-CLIP-ViT-G/14</td>
      <td>Vicuna-7B</td>
      <td>Q-Former</td>
      <td>Memory Bank Compression</td>
      <td>Merging adjacent frames</td>
      <td>100</td>
      <td>/32</td>
      <td>4 A100</td>
      <td>E2E</td>
      <td>E2E</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2404.16994">PLLaVA</a></td>
      <td>23.04</td>
      <td>CLIP-ViT-L/14</td>
      <td>LLaVA-Next-LLM</td>
      <td colspan="3" style="text-align:center;">Adaptive Pooling</td>
      <td>64</td>
      <td>2304</td>
      <td>-</td>
      <td>Y-N-N</td>
      <td>Y-Y-N</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2404.03384">LongVLM</a></td>
      <td>23.04</td>
      <td>CLIP-ViT-L/14</td>
      <td>Vicuna1.1-7B</td>
      <td colspan="3" style="text-align:center;">Hierarchical token merging</td>
      <td>100</td>
      <td>/305</td>
      <td>4 A100 80G</td>
      <td>Y-N-N</td>
      <td>Y-Y-N</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2404.03413">MiniGPT4-Video</a></td>
      <td>24.04</td>
      <td>EVA-CLIP-ViT-G/14</td>
      <td>LLaMA2-7B, Mistral-7B</td>
      <td>Merging adjacent tokens</td>
      <td>--</td>
      <td>--</td>
      <td>90</td>
      <td>64/5760</td>
      <td>-</td>
      <td>Y-Y-N</td>
      <td>N-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2404.11865">RED-VILLM</a></td>
      <td>24.04</td>
      <td>Openclip-ViT-bigG</td>
      <td>Qwen-7B</td>
      <td>Spatial pooling</td>
      <td>Temporal pooling</td>
      <td>--</td>
      <td>100</td>
      <td>/1124</td>
      <td>-</td>
      <td>Y-N-N</td>
      <td>Y-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2404.00308">ST-LLM</a></td>
      <td>24.04</td>
      <td>BLIP-2</td>
      <td>InstructBLIP-Vicuna1.1-7B</td>
      <td>Q-Former</td>
      <td>Masked video modeling</td>
      <td>Global-Local input</td>
      <td>16</td>
      <td>/512</td>
      <td>8 A100</td>
      <td>E2E</td>
      <td>E2E</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://llava-vl.github.io/blog/2024-04-30-llava-next-video/">LLaVA-NeXT-Video</a></td>
      <td>24.04</td>
      <td>CLIP-ViT-L/14</td>
      <td>Vicuna1.5-7B/13B, Nous-Hermes-2-Yi-34B</td>
      <td>Merging adjacent tokens</td>
      <td>--</td>
      <td>--</td>
      <td>32</td>
      <td>4608</td>
      <td>-</td>
      <td>Y-Y-N</td>
      <td>Y-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2405.01483">Mantis-Idefics2</a></td>
      <td>24.05</td>
      <td>SigLIP-SO400M</td>
      <td>Mistral0.1-7B</td>
      <td>Perceiver resampler</td>
      <td>--</td>
      <td>--</td>
      <td>8</td>
      <td>64/512</td>
      <td>16 A100-40G</td>
      <td>Y-N-N</td>
      <td>N-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2406.07476">VideoLLaMA 2</a></td>
      <td>24.06</td>
      <td>CLIP-ViT-L/14</td>
      <td>Mistral-7B-Instruct</td>
      <td colspan="2" style="text-align:center;">Spatial-Temporal Convolution</td>
      <td>--</td>
      <td>8</td>
      <td>/576</td>
      <td>-</td>
      <td>Y-Y-N</td>
      <td>Y-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2406.16852">LongVA</a></td>
      <td>24.06</td>
      <td>CLIP-ViT-L/14</td>
      <td>Qwen2-7B-224K</td>
      <td>Merging adjacent tokens</td>
      <td>Expanding tokens</td>
      <td>--</td>
      <td>384</td>
      <td>55,296</td>
      <td>8x A100-80G</td>
      <td>-</td>
      <td>Y-N-N</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2406.00258">Artemis</a></td>
      <td>24.06</td>
      <td>CLIP-ViT-L/14</td>
      <td>Vicuna1.5-7B</td>
      <td colspan="3" style="text-align:center;">Average pooling</td>
      <td>5</td>
      <td>/356</td>
      <td>8 x A800</td>
      <td>Y-Y-N</td>
      <td>N-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2406.09418">VideoGPT+</a></td>
      <td>24.06</td>
      <td>CLIP-ViT-L/14, InternVideo-v2</td>
      <td>Phi3-Mini-3.8B</td>
      <td>Adaptive pooling</td>
      <td>Adaptive pooling</td>
      <td>--</td>
      <td>16</td>
      <td>/2560</td>
      <td>8 x A100 40G</td>
      <td>Y-Y-N</td>
      <td>N-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2412.09596?">IXC-2.5</a></td>
      <td>24.07</td>
      <td>CLIP-ViT-L/14-490</td>
      <td>InternLM2-7B</td>
      <td>Merging adjacent tokens</td>
      <td>Expanding tokens</td>
      <td>Frame index</td>
      <td>64</td>
      <td>400/25600</td>
      <td>-</td>
      <td>Y-Y-N</td>
      <td>Y-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2407.14177">EVLM</a></td>
      <td>24.07</td>
      <td>EVA2-CLIP-E-Plus</td>
      <td>Qwen-14B-Chat 1.0</td>
      <td>Gated cross attention</td>
      <td>--</td>
      <td>--</td>
      <td>--</td>
      <td>/16</td>
      <td>-</td>
      <td>Y-Y-N</td>
      <td>Y-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2407.15841?">SlowFast-LLaVA</a></td>
      <td>24.07</td>
      <td>CLIP-ViT-L/14</td>
      <td>Vicuna1.5-7B</td>
      <td>Merging adjacent tokens</td>
      <td colspan="2" style="text-align:center;">Slow and fast pathway</td>
      <td>50</td>
      <td>3680</td>
      <td>A100-80G</td>
      <td>-</td>
      <td>-</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2407.07895">LLaVA-Interleave</a></td>
      <td>24.07</td>
      <td>SigLIP-SO400M</td>
      <td>Qwen1.5-0.5B/7B/14B</td>
      <td>--</td>
      <td>--</td>
      <td>--</td>
      <td>16</td>
      <td>729/11664</td>
      <td>-</td>
      <td>Y-N-N</td>
      <td>Y-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2408.15542">Kangaroo</a></td>
      <td>24.08</td>
      <td>EVA-CLIP-ViT-G/14</td>
      <td>LLaMA3-8B</td>
      <td colspan="3" style="text-align:center;">3D Depthwise convolution</td>
      <td>--</td>
      <td>--</td>
      <td>-</td>
      <td>Y-Y-N</td>
      <td>Y-Y-Y</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2408.05211?">VITA</a></td>
      <td>24.08</td>
      <td>InternViT-300M-448px</td>
      <td>Mixtral 8x7B</td>
      <td>MLP</td>
      <td>--</td>
      <td>--</td>
      <td>16</td>
      <td>256/4096</td>
      <td>-</td>
      <td>Y-Y-N</td>
      <td>Y-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2408.03326?">LLaVA-OneVision</a></td>
      <td>24.08</td>
      <td>SigLIP-SO400M</td>
      <td>Qwen2-7B</td>
      <td>Merging adjacent tokens</td>
      <td>--</td>
      <td>--</td>
      <td>1 fps</td>
      <td>729/</td>
      <td>-</td>
      <td>Y-N-N</td>
      <td>Y-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2408.10188">LONGVILA</a></td>
      <td>24.08</td>
      <td>SigLIP-SO400M</td>
      <td>Qwen2-1.5B/7B</td>
      <td colspan="3" style="text-align:center;">Multi-Modal Sequence Parallelism</td>
      <td>1024</td>
      <td>256/</td>
      <td>256 A100 80G</td>
      <td>Y-Y-N</td>
      <td>Y-Y-Y</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2409.02889?">LongLLaVA</a></td>
      <td>24.09</td>
      <td>CLIP-ViT-B/32</td>
      <td>LLaVA1.6-13B</td>
      <td>Merging adjacent tokens</td>
      <td>Mamba Layers</td>
      <td>Hybrid architecture</td>
      <td>256</td>
      <td>144/</td>
      <td>24 A800 80G</td>
      <td>Y-N-N</td>
      <td>Y-Y-N</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/2409.12191">Qwen2-VL</a></td>
      <td>24.09</td>
      <td>CLIP-ViT-L/14</td>
      <td>Qwen2-1.5B/7B/72B</td>
      <td>Merging adjacent tokens</td>
      <td>3D convolutions</td>
      <td>--</td>
      <td>2 fps</td>
      <td>66/</td>
      <td>-</td>
      <td>Y-N-N</td>
      <td>Y-Y-N</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2409.14485">Video-XL</a></td>
      <td>20.09</td>
      <td>CLIP-ViT-L/14</td>
      <td>Qwen-2-7B</td>
      <td>Merging adjacent tokens</td>
      <td colspan="2" style="text-align:center;">Visual Summarization Token and Dynamic Compression</td>
      <td>128</td>
      <td>--</td>
      <td>8 A800-80G</td>
      <td>Y-N-N</td>
      <td>Y-Y-N</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2409.12961">Oryx-1.5</a></td>
      <td>24.10</td>
      <td>OryxViT</td>
      <td>Qwen-2.5-7B/32B</td>
      <td>Variable-Length Self-Attention</td>
      <td colspan="2" style="text-align:center;">Dynamic Compressor</td>
      <td>64</td>
      <td>256/</td>
      <td>64 A800-80G</td>
      <td>Y-Y-N</td>
      <td>Y-Y-Y</td>
      <td>No</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2411.18211">TimeMarker</a></td>
      <td>24.11</td>
      <td>LLaVA-Encoder</td>
      <td>LLaVA-LLM</td>
      <td colspan="3" style="text-align:center;">Adaptive Token Merge and Temporal Separator Tokens Integration</td>
      <td>128</td>
      <td>--</td>
      <td>-</td>
      <td>Y-Y-N</td>
      <td>Y-Y-Y</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/pdf/2412.04468">NVILA</a></td>
      <td>24.12</td>
      <td>SigLIP-SO400M</td>
      <td>Qwen2-7B/14B</td>
      <td>Spatial-to-Channel Reshaping</td>
      <td colspan="2" style="text-align:center;">Temporal Averaging</td>
      <td>256</td>
      <td>/8192</td>
      <td>128 H100-80G</td>
      <td>Y-Y-N</td>
      <td>Y-Y-Y</td>
      <td>Yes</td>
    </tr>
  </tbody>
</table>

## Long video understanding benchmarks
1. **Video-MME**: Popular video understanding evaluation benchmark, including short, medium, and long video resources with 900 videos and 2,700 annotations. The average duration is 17.0 minutes. [Project](https://video-mme.github.io/home_page.html), [GitHub](https://github.com/BradyFU/Video-MME), [Dataset](https://github.com/BradyFU/Video-MME?tab=readme-ov-file#-dataset), [Paper](https://arxiv.org/pdf/2405.21075)

2. **HourVideo**: Hour-level video understanding evaluation benchmark, including long video resources of 500 videos and 12,976 annotations. The average duration is 45.7 minutes. [Project](https://hourvideo.stanford.edu/), [GitHub](https://github.com/keshik6/HourVideo), [Dataset](https://huggingface.co/datasets/HourVideo/HourVideo), [Paper](https://arxiv.org/abs/2411.04998)

3. **HLV-1K**: Hour-level video understanding evaluation benchmark, including long video resources of 1,009 videos and 14,847 annotations. The average duration is 55.0 minutes. [Project](https://vincent-zhq.github.io/hlv-1k-project/), [GitHub](https://github.com/Vincent-ZHQ/HLV-1K), [Dataset](https://github.com/Vincent-ZHQ/HLV-1K), [Paper](https://arxiv.org/submit/6108440/view)

4. **LVBench**: Hour-level video understanding evaluation benchmark, including long video resources of 103 videos and 1,549 annotations. The average duration is 68.4 minutes. [Project](https://lvbench.github.io/), [GitHub](https://github.com/THUDM/LVBench), [Dataset](https://huggingface.co/datasets/THUDM/LVBench), [Paper](https://arxiv.org/pdf/2406.08035)



## Performance on long video benchamarks
<img width="969" alt="image" src="https://github.com/user-attachments/assets/fb0aa46a-e413-4eb5-9841-015e56679672"/>

## Performance on common video benchmarks

<img width="946" alt="image" src="https://github.com/user-attachments/assets/9c652905-c3ba-4095-b5c3-b34f314518ca" />


### citation
If you use our code or find our CA-MSER useful in your research, please consider citing:

    @article{zou2024seconds,
      title={From Seconds to Hours: Reviewing MultiModal Large Language Models on Comprehensive Long Video Understanding},
      author={Zou, Heqing and Luo, Tianze and Xie, Guiyang and Lv, Fengmao and Wang, Guangcong and Chen, Juanyang and Wang, Zhuochen and Zhang, Hansheng and Zhang, Huaijian and others},
      journal={arXiv preprint arXiv:2409.18938},
      year={2024}
    }
