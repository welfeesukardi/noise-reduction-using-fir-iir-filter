# *Bahasa Indonesia* &mdash; Indonesian (`id`)

This datasheet is for cv-corpus-27.0-2026-09-11 of the Mozilla Common Voice *Scripted Speech* dataset for Indonesian [Bahasa Indonesia - `id`]. The dataset contains 60923 clips representing 67.53 hours of recorded speech (34.25 hours validated) from 678 speakers, recorded from a text corpus of 25,186 sentences.

## Language

### Accents

| Code | Accent | Clips | Speakers |
|---|---|---|---|
| - |  | 5,565 (9.1%) | 60 (8.8%) |

## Demographic information

The dataset includes the following self-declared age and gender distributions. A coverage summary is shown below each table.

### Gender

Self-declared gender information. The table shows clip and speaker counts with percentages. Speakers who did not declare a gender are listed as Unspecified. A dash (-) indicates zero.

| Code | Gender | Clips | Speakers |
|---|---|---|---|
| male_masculine | Male, masculine | 26,420 (43.4%) | 191 (28.2%) |
| female_feminine | Female, feminine | 15,693 (25.8%) | 52 (7.7%) |
| transgender | Transgender | - | - |
| non-binary | Non-binary | - | - |
| do_not_wish_to_say | Prefer not to say | 10 (0.0%) | 1 (0.1%) |
| - | Unspecified | 18,795 (30.9%) | 472 (69.6%) |

*Gender declared: 42,128 of 60,923 clips (69.1%), 206 of 678 speakers (30.4%)*

### Age

Self-declared age information. The table shows clip and speaker counts with percentages. Speakers who did not declare an age are listed as Unspecified. A dash (-) indicates zero.

| Code | Age | Clips | Speakers |
|---|---|---|---|
| teens | Teens | 12,808 (21.0%) | 39 (5.8%) |
| twenties | Twenties | 25,306 (41.5%) | 159 (23.5%) |
| thirties | Thirties | 6,177 (10.1%) | 49 (7.2%) |
| fourties | Fourties | 1,046 (1.7%) | 20 (2.9%) |
| fifties | Fifties | 234 (0.4%) | 3 (0.4%) |
| sixties | Sixties | - | - |
| seventies | Seventies | - | - |
| eighties | Eighties | - | - |
| nineties | Nineties | - | - |
| - | Unspecified | 15,352 (25.2%) | 452 (66.7%) |

*Age declared: 45,571 of 60,923 clips (74.8%), 226 of 678 speakers (33.3%)*

## Data splits for modelling

**Clip buckets**

| Bucket | Clips |
|---|---|
| Validated | 30,901 (50.7%) |
| Invalidated | 2,835 (4.7%) |
| Other | 27,187 (44.6%) |

**Training splits**

| Split | Clips |
|---|---|
| Train | 4,999 (16.2%) |
| Dev | 3,497 (11.3%) |
| Test | 3,711 (12.0%) |

*Training split coverage: 12,207 of 30,901 validated clips (39.5%)*

The dataset contains 30901 validated, 2835 invalidated, and 27187 unresolved clips. The average clip duration is 3.991 seconds.

## Text corpus

**Validated sentences:** 13,472

| Category | Count |
|---|---|
| Unvalidated sentences | 11,714 |
| Pending sentences | 11,696 |
| Rejected sentences | 18 |
| Reported sentences | 364 |

The corpus contains 25,186 sentences: 13,472 validated and 11,714 unvalidated (11,696 pending review, 18 rejected), with 364 reported for review.

### Sample

There follows a randomly selected sample of five sentences from the corpus.

1. *Saya sangat suka kue yang manis.*
2. *Semua orang dipersilahkan.*
3. *Mereka akan mati.*
4. *Mohon tunggu giliran Anda.*
5. *Sekarang ini saya sedang makan malam.*

### Sources

| Source | Sentences |
|---|---|
| covost2-en_id | 6,465 (48.0%) |
| sentence-collector | 6,240 (46.3%) |
| http://tatoeba.org | 351 (2.6%) |
| example sentences from dictionaries | 156 (1.2%) |
| Other | 260 (1.9%) |

### Fields

#### Clips

Each row of a `tsv` file represents a single audio clip, and contains the following information:

- `client_id` - hashed UUID of a given user
- `path` - relative path of the audio file
- `sentence` - the sentence to be read aloud
- `sentence_id` - unique identifier for the sentence
- `sentence_domain` - domain classification(s) of the sentence
- `up_votes` - number of people who said audio matches the text
- `down_votes` - number of people who said audio does not match text
- `age` - age of the speaker[^1]
- `gender` - gender of the speaker[^1]
- `accents` - accents of the speaker[^1]
- `variant` - variant of the language[^1]
- `locale` - locale code of the language
- `segment` - if sentence belongs to a custom dataset segment, it will be listed here

[^1]: For a full list of age, gender, and accent options, see the [demographics spec](https://github.com/common-voice/common-voice/blob/main/web/src/stores/demographics.ts). These will only be reported if the speaker opted in to provide that information.

#### `validated_sentences.tsv`

The `validated_sentences.tsv` file contains one row per validated sentence in the text corpus:

- `sentence_id` - unique identifier for the sentence
- `sentence` - the sentence text
- `variant` - the variant of the language
- `sentence_domain` - the domain(s) the sentence belongs to
- `source` - the source the sentence was collected from
- `is_used` - whether the sentence is still in circulation for recording
- `clips_count` - number of clips recorded for this sentence

#### `unvalidated_sentences.tsv`

The `unvalidated_sentences.tsv` file contains one row per unvalidated sentence in the text corpus:

- `sentence_id` - unique identifier for the sentence
- `sentence` - the sentence text
- `variant` - the variant of the language
- `sentence_domain` - the domain(s) the sentence belongs to
- `source` - the source the sentence was collected from
- `up_votes` - number of upvotes the sentence received
- `down_votes` - number of downvotes the sentence received
- `status` - current status of the sentence (`pending` or `rejected`)

## Get involved

### Community links

- [Common Voice translators on Pontoon](https://pontoon.mozilla.org/id/common-voice/contributors/)
- [Common Voice Communities](https://github.com/common-voice/common-voice/blob/main/docs/COMMUNITIES.md)

### Discussions

- [Common Voice on Matrix](https://chat.mozilla.org/#/room/#common-voice:mozilla.org)
- [Common Voice on Discourse](https://discourse.mozilla.org/t/about-common-voice-readme-first/17218)
- [Common Voice on Discord](https://discord.gg/9QTj9zwn)
- [Common Voice on Telegram](https://t.me/mozilla_common_voice)

### Contribute

- [Speak](https://commonvoice.mozilla.org/id/speak)
- [Write](https://commonvoice.mozilla.org/id/write)
- [Listen](https://commonvoice.mozilla.org/id/listen)
- [Review](https://commonvoice.mozilla.org/id/review)

## Licence

This dataset is released under the [Creative Commons Zero (CC-0)](https://creativecommons.org/public-domain/cc0/) licence. By downloading this data you agree to not determine the identity of speakers in the dataset.
