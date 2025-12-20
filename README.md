---
license: mit
language:
- en
tags:
- epstein
- epstein-data
- dataset
- fbi
- journalism
---

# FULL_EPSTEIN_INDEX

<div style="padding: 0.75rem 1rem; border-radius: 0.5rem; background-color: #2f0000; color: #ffd4d4; font-weight: 600; border: 1px solid #ff9999;">
CONTENT WARNING: This repository contains graphic and highly sensitive material regarding sexual abuse, exploitation, trafficking, and violence. It also contains unverified allegations and raw witness statements. User discretion is strongly advised.
</div>

## Overview

**FULL_EPSTEIN_INDEX** is a comprehensive, unified research archive aggregating public releases related to the Jeffrey Epstein estate and associated investigations. 

This repository expands upon earlier archives (such as the initial November 2025 House Oversight release) by integrating the **First Phase of Declassified Epstein Files** released by the Department of Justice. Unlike previous datasets restricted to scanned emails, this index combines:

1.  **House Oversight Documents:** ~20,000 pages of emails and estate records (Nov 2025).
2.  **DOJ Disclosures:** Flight logs, contact books (redacted), and the "Masseuse List."
3.  **Multimedia Evidence:** BOP video footage and audio recordings from the Maxwell Proffer sessions.
4.  **Transcripts:** Auto-generated text transcripts for all audio and video files to enable full-text search.

**Note on Updates:** This index is a living archive. As additional phases of files are declassified and released by government bodies, they will be processed, indexed, and added to this repository.

## Dataset Contents

The repository is organized to facilitate open-source intelligence (OSINT) analysis and research:

* `FULL_EPSTEIN_INDEX.csv`: The master index containing the text content of **all** files. This allows for a single, unified search across PDFs, images, and video transcripts.
* `raw_files/`: The original source files, preserved in their native formats:
    * **Documents:** PDFs of flight logs, contact books, and legal evidence lists.
    * **Video:** MP4 files of BOP facility footage (Aug 2019) and other evidence.
    * **Audio:** WAV files of witness interviews and proffer sessions.
* `transcripts/`: (Optional) Individual text files for specific media assets.

## Preprocessing & Methodology

To make this heterogeneous dataset searchable, we employed the following pipeline:

* **Legacy Documents:** Text from the original 20k document release was preserved from the original OCR extraction.
* **New PDFs:** Processed using `pdfplumber` to extract high-fidelity text from digital-native government releases (e.g., flight logs).
* **Audio & Video:** Transcribed using **OpenAI Whisper** (Base model). 
    * *Note:* Transcripts are automated and may contain errors, especially with low-quality audio or overlapping speech. Always cross-reference with the original `raw_files` media.

## Usage Guidelines

This dataset is intended for **research, investigative journalism, and legal analysis**. By accessing this repository, you agree to the following ethical guidelines:

### User Responsibilities
* **Verify Facts:** Much of this data consists of raw evidence, notes, and unverified allegations. Do not present search results as established fact without corroboration.
* **Respect Privacy:** Adhere to all redactions found in the source documents. Do not attempt to use this data to doxx or harass individuals.
* **Victim Dignity:** Treat all information regarding potential victims with extreme care and respect.

### Prohibited Uses
* **No Fine-Tuning:** Do not use this dataset to train or fine-tune generative AI models. The risk of generating hallucinations regarding sensitive legal matters is too high.
* **No Harassment:** Do not use this tool to target private individuals.
* **No Commercial Exploitation:** This data is for public interest and educational purposes.

## Sources

This index aggregates public domain releases from:
1.  **U.S. House Committee on Oversight and Accountability** (Nov 12, 2025 Release)
2.  **U.S. Department of Justice** (First Phase Declassification, Flight Logs, Maxwell Proffer Material, Dec 2025 Release)

## Legal & Disclaimer

**Disclaimer:** This repository is an independent collection and is not an official service of the U.S. Government. 

* **Copyright:** Original government documents are generally in the public domain or released under Fair Use principles for research. The organizing scripts and index structure are licensed under the MIT License.
* **Liability:** The maintainers of `FULL_EPSTEIN_INDEX` claim no ownership over the underlying documents and assume no liability for the use, misuse, or interpretation of this data. Users are solely responsible for compliance with applicable laws and privacy regulations.

---

*To contribute corrections to transcripts or metadata, please open a Pull Request citing the specific File ID.*
