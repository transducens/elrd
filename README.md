# English Learners Role-Playing Dialogue Dataset (ELRD)

A dataset featuring audio recordings and diarized, automatically-obtained transcriptions from role-playing video calls with L1-Spanish/L2-English learners. Role-playing games help avoid the difficulties associated with anonymizing real online meetings and allowed us to control the topics and complexity of the conversations.

## Overview

The English Learners Role-Playing Dialogue (ELRD) dataset was released as a result of the human evaluation carried out in the [DeMINT](https://github.com/transducens/demint) project developed at Universitat d'Alacant, Spain. The objective of DeMINT was to develop a chatbot that helps non-native English speakers improve their language skills by analyzing and providing feedback on the transcripts of their online meetings. 

The evaluation involved interactions between the chatbot and a group of L1-Spanish/L2-English students. These students were recruited through our university’s Language Services, which maintains a pool of individuals registered for multilingualism-related activities. From those willing to participate, seven students were selected, each dedicating approximately 10 hours to evaluation activities. We specifically targeted students with English proficiency levels of B2/C1, as defined by the Common European Framework of Reference for Languages (CEFR), and sought a balanced group in terms of gender and diversity.

To facilitate this evaluation, fifteen video calls of around 10 minutes each were organized, involving two or three participants per call. These calls utilized role-playing activities, carefully chosen to engage students in English conversation. Role-playing games not only allow us to control the conversation topics and complexity, but also circumvent the challenges associated with anonymizing real online meetings. For these sessions, we used the role-play scenarios from "ESL Role Plays: 50 Engaging Role Plays for ESL and EFL Classes" by Larry Pitts (ECQ Publishing, 2015). This book provides detailed contexts for role-playing activities, along with preparatory questions to help students familiarize themselves with each scenario. After the students prepared for their meetings, the video calls were recorded, and they later participated in debriefing sessions with our chatbot to review and analyze errors in their English usage during the calls. This repository includes the audio recordings and the corresponding diarized, automatically-obtained transcriptions.

## Dataset Content

### 1. Audio Recordings

- Folder: `audios/`
- This folder contains the audio recordings of the video calls in `.wav` format.
- Each file is named according to the role-playing scenario and the participants involved. For example, `meeting-camping-dm01-dm04-dm05.wav` refers to a meeting in which three speakers (dm01, dm04, and dm05) participated, playing the "camping" role-playing game.

### 2. Diarized Transcripts

- Folder: `diarized_transcripts/`
- This folder contains the diarized transcripts in `.jsonl` format, where each transcript is segmented according to the speaker.
- The names of the files in this folder correspond to the audio recordings, with the same structure but a `.jsonl` extension instead of `.wav`. For example, `meeting-camping-dm01-dm04-dm05.jsonl` contains the diarized transcript for the corresponding audio file.
  
### File Naming Convention

Each file is named following this structure:

- `meeting-[roleplay]-[speakerID].wav` / `.jsonl`
- `roleplay`: The name of the role-playing game used during the meeting, as documented in the `roleplay-descriptions.md` file in the repository. For example, "camping" refers to the specific game the participants played.
- `speakerID`: Each participant is assigned an ID (e.g., `dm01`, `dm04`, `dm05`) that identifies them throughout the conversation.

### Role-Playing Activites

The role-playing activities are documented in detail in the file `roleplay-descriptions.md`, providing context for the different scenarios and instructions followed by the participants.

## Citation
If you use this dataset in your research, please cite the following paper in addition to this repository:

```bibtex
@inproceedings{demint2024,
  author = {Pérez-Ortiz, Juan Antonio and 
    Esplà-Gomis, Miquel and 
    Sánchez-Cartagena, Víctor M. and 
    Sánchez-Martínez, Felipe and 
    Chernysh, Roman and 
    Mora-Rodríguez, Gabriel and 
    Berezhnoy, Lev},
  title = {{DeMINT}: Automated Language Debriefing for English Learners via {AI} 
           Chatbot Analysis of Meeting Transcripts},
  booktitle = {Proceedings of the 13th Workshop on NLP for Computer Assisted Language Learning},
  month = october,
  year = {2024},
  url = {https://aclanthology.org/volumes/2024.nlp4call-1/},
}
