# LLM_vicuna_fine_tuning
Fine tuning of Large Lenguage Model Vicuna for "What? Where? When?" (русск. Что? Где? Когда?) game.

## Dataset: База вопросов «Что? Где? Когда?» https://db.chgk.info/

## Weights
Initial weights: https://huggingface.co/helloollel/vicuna-13b

Adapters weights after finetunning /adapters-weights/vicuna-13b_checkpoint_LoRA_chk200/, LoRA config:

peft_config = LoraConfig(
    r=128,
    lora_alpha=24,
    target_modules=["q_proj", "v_proj", "v_proj", "o_proj", "gate_proj", "down_proj"],
    lora_dropout=0.0,
    bias="lora_only",
    task_type="CAUSAL_LM",
)
