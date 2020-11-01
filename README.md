# Neural Interview Audiolizer

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/olaviinha/NeuralInterviewAudiolizer/blob/main/NeuralInterviewAudiolizer.ipynb)

Neural Interview Audiolizer is a ".txt to .wav" notebook that turns textual dialogue (e.g. interview, chat) of two individuals to audio dialogue using [Google Cloud Text-to-Speech API](https://cloud.google.com/text-to-speech). It uses two selectable and configurable WaveNet voices.

It was made to run in [Google Colaboratory](https://colab.research.google.com/) (i.e. your browser), using [your Google Drive](https://drive.google.com/drive/my-drive) as data source and storage.

**Note** that using this notebooks requires access to Google's Text-to-Speech API with an API key. See [this page](https://cloud.google.com/text-to-speech/docs/quickstart-client-libraries#before-you-begin) for more information on how to obtain access.

**Two dialogue formats are supported:**
1) `question_and_answer` expects an empty line between every time speaker changes.
2) `dialogue_with_names` expects `Name:` (e.g. _John: Hello Bob! How are you?_) every time speaker changes. Speaker is changed despite the name in the beginning, will probably improve this later to take names into account.

See the notebook for more details.

## Audio demos

Source text | Result
------------ | ------------
[gpt-3_chat-1.txt](https://storage.googleapis.com/olaviinha/github/neural-interview-audiolizer/gpt-3_chat-1.txt) | [gpt-3_chat-1.wav](https://storage.googleapis.com/olaviinha/github/neural-interview-audiolizer/gpt-3_chat-1.wav)
