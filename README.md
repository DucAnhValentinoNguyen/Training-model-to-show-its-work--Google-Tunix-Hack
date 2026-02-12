# Training-model-to-show-its-work--Google-Tunix-Hack
Kaggle competition: fine-tune Google’s open-weight Gemma model (Gemma2 2B or Gemma3 1B) with Tunix on TPU, and teach it how to reason through complex questions: create a model that not only gets the right answer, but also explains how it got there.

A working training pipeline using Tunix and Gemma.

Kaggle Writeup: includes a title, subtitle, and a detailed analysis:
a. Media Gallery
images and/or videos associated with submission. A cover image is required to submit Writeup.

b. Public Notebook

c. Video
Attach video to the Media Gallery. 
Videos should be 3 minutes or less, and should be published to Youtube.

he notebook is clearly written and detailed with:
- Training data
- Hyperparameters
- Prompt
- Training strategy and techniques.

A Gemma2 starter notebook for math reasoning can be found here (Kaggle-hosted version).

Given limited compute on Kaggle TPUs (9 hours per session, 20 hours per week):
- Max output token <1K is fine
- English-only. Multilinguality is not the focus of this hackathon.
- Tool use is not necessary.
- No multimodality

- The fine tuned model is the direct output from the notebook above and runs on a single Kaggle TPU session (9 hours).
- The generated model checkpoint files must be loadable and runnable via the Gemma2 or Gemma3 modeling code in Tunix on Kaggle.
- Model output should follow this format:
<reasoning>model_thinking_trace</reasoning>
<answer>model_answer</answer>

Evaluation will cover both the reasoning trace and the final answer, and be done via a combination of LLM-as-a-judge and human judgment. Eval user queries are held out during the hackathon and may come from a range of verifiable and non-verifiable domains, including but not limited to:
- Creative writing
- Creative ideation
- Summarization
- Math
- Coding
- Basic science
- Other
