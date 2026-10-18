---
layout: page
title: research
permalink: /research/
description: Technical reports and research papers.
nav: true
nav_order: 2
_styles: |
  .research-report {
    display: flex;
    align-items: flex-start;
    gap: 1.5rem;
    margin: 1.5rem 0 2.5rem;
  }
  .research-report + .research-report {
    padding-top: 2rem;
    border-top: 1px solid var(--global-divider-color);
  }
  .research-report__cover {
    display: block;
    flex: 0 0 200px;
    width: 200px;
    max-width: 100%;
  }
  .research-report__cover img {
    display: block;
    width: 100%;
    height: auto;
    background: white;
    border: 1px solid var(--global-divider-color);
  }
  .research-report__details {
    min-width: 0;
    overflow-wrap: anywhere;
  }
  .research-report__details h3 {
    margin: 0 0 0.75rem;
    font-size: 1.4rem;
    line-height: 1.35;
    font-weight: 500;
  }
  .research-report__details p {
    max-width: 65ch;
    line-height: 1.65;
    margin-bottom: 1rem;
  }
  .research-report__pdf {
    display: inline-flex;
    align-items: center;
    min-height: 44px;
    padding: 0.4rem 0.85rem;
    border: 1px solid currentColor;
    border-radius: 4px;
    font-size: 0.9rem;
    font-weight: 500;
  }
  .research-report__pdf:hover {
    background-color: var(--global-code-bg-color);
  }
  .research-report a:focus-visible {
    outline: 2px solid var(--global-theme-color);
    outline-offset: 4px;
  }
  @media (max-width: 575.98px) {
    .research-report {
      flex-direction: column;
      gap: 1rem;
    }
    .research-report__cover {
      flex-basis: auto;
    }
  }
---

## Technical Reports

<div class="research-report">
  <a class="research-report__cover" href="{{ '/assets/pdf/technical-reports/what-does-gpt-2-look-at.pdf' | relative_url }}">
    <img src="{{ '/assets/img/technical-report/what-does-gpt-2-look-at.png' | relative_url }}" alt="First page of What Does GPT-2 Look At?" width="800" height="1036" loading="lazy">
  </a>
  <div class="research-report__details">
    <h3>What Does GPT-2 Look At?</h3>
    <p>
      Understanding the attention patterns of pretrained language models can help characterize their internal behavior. Inspired by prior
      analyses of BERT, we examine relative-position preferences, attention to token categories, attention entropy, and head similarity in
      GPT-2 Small. Across 1,000 Wikipedia segments, we identify five heads that assign more than half their attention to the current token
      and two that strongly prefer the preceding token. Many heads in intermediate and deeper layers attend heavily to an initial
      end-of-text (EOT) token, whereas non-boundary tokens assign almost no attention to natural paragraph boundaries. Entropy is relatively high
      in early layers, and trailing-EOT queries exhibit a distinct layer-dependent trend. Finally, a two-dimensional embedding reveals
      clusters associated with different attention patterns, with earlier-layer heads generally more dispersed than later-layer heads.
    </p>
    <a class="research-report__pdf" href="{{ '/assets/pdf/technical-reports/what-does-gpt-2-look-at.pdf' | relative_url }}" aria-label="Read What Does GPT-2 Look At? (PDF)">Read report (PDF)</a>
  </div>
</div>

<div class="research-report">
  <a class="research-report__cover" href="{{ '/assets/pdf/technical-reports/revisiting-titanfuzz.pdf' | relative_url }}">
    <img src="{{ '/assets/img/technical-report/revisiting-titanfuzz.png' | relative_url }}" alt="First page of Revisiting TitanFuzz: A Reproduction and Comparative Evaluation Against DeepREL" width="800" height="1036" loading="lazy">
  </a>
  <div class="research-report__details">
    <h3>Revisiting TitanFuzz: A Reproduction and Comparative Evaluation Against DeepREL</h3>
    <p>
      Testing deep learning frameworks has long been a challenging task. TitanFuzz introduces an LLM-based fuzzing approach that combines
      autoregressive code generation and code infilling to generate diverse test programs. In this study, we reproduce TitanFuzz and
      evaluate its effectiveness against DeepREL, an API-level fuzzer, on PyTorch. We select 30 APIs across six categories and conduct ten
      independent runs per API for each fuzzer, with a fixed time budget of 60 seconds per run. By independently replaying up to 50
      generated candidates per run, we measure additional PyTorch Python source lines, previously unseen ATen operator names, valid test
      yield, and potential bugs. On average, TitanFuzz covers 22.75 additional Python lines and 17.54 new ATen operator names per API–run,
      compared with 3.44 and 13.21 for DeepREL. However, TitanFuzz produces a lower valid yield (50.69% versus 68.42%). These results
      highlight a trade-off between broader program exploration and test validity.
    </p>
    <a class="research-report__pdf" href="{{ '/assets/pdf/technical-reports/revisiting-titanfuzz.pdf' | relative_url }}" aria-label="Read Revisiting TitanFuzz (PDF)">Read report (PDF)</a>
  </div>
</div>
