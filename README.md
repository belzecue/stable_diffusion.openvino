# stable_diffusion.openvino

Implementation of Text-To-Image generation using Stable Diffusion on Intel CPU.
<p align="center">
  <img src="data/title.png"/>
</p>

## Requirements

* Linux, Windows, MacOS
* Python 3.8.+
* CPU compatible with OpenVINO.

## Install requirements

```bash
pip install -r requirements.txt
```

## Generate image from text description

```bash
usage: stable_diffusion.py [-h] [--model MODEL] [--seed SEED] [--beta-start BETA_START] [--beta-end BETA_END] [--beta-schedule BETA_SCHEDULE] [--num-inference-steps NUM_INFERENCE_STEPS]
                           [--guidance-scale GUIDANCE_SCALE] [--eta ETA] [--tokenizer TOKENIZER] [--prompt PROMPT] [--output OUTPUT]

optional arguments:
  -h, --help            show this help message and exit
  --model MODEL         model name
  --seed SEED           random seed for generating consistent images per prompt
  --beta-start BETA_START
                        LMSDiscreteScheduler::beta_start
  --beta-end BETA_END   LMSDiscreteScheduler::beta_end
  --beta-schedule BETA_SCHEDULE
                        LMSDiscreteScheduler::beta_schedule
  --num-inference-steps NUM_INFERENCE_STEPS
                        num inference steps
  --guidance-scale GUIDANCE_SCALE
                        guidance scale
  --eta ETA             eta
  --tokenizer TOKENIZER
                        tokenizer
  --prompt PROMPT       prompt
  --output OUTPUT       output image name
```

### Example
```bash
python stable_diffusion.py --prompt "Street-art painting of Emilia Clarke in style of Banksy, photorealism"
```

## Performance

| CPU                                      | Time per iter | Total time |
|------------------------------------------|---------------|------------|
| Intel(R) Core(TM) i5-8279U               | 7.4 s/it      | 3.59 min   |
| AMD Ryzen Threadripper 1900X             | 5.34 s/it     | 2.58 min   |
| Intel(R) Xeon(R) Gold 6154 CPU @ 3.00GHz | 1 s/it        | 33 s       |
| Intel(R) Core(TM) i7-1165G7 @ 2.80GHz    | 7.4 s/it      | 3.59 min   |

## Acknowledgements

* Original implementation of Stable Diffusion: https://github.com/CompVis/stable-diffusion
* diffusers library: https://github.com/huggingface/diffusers

## Disclaimer

The authors are not responsible for the content generated using this project.
Please, don't use this project to produce illegal, harmful, offensive etc. content.
