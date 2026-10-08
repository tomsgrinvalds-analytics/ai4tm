# AI4TM - AI for Marketing Masterclass

Content, notebooks, and guides for the AI for Marketing (AI4TM) masterclass — 6 weeks covering AI fundamentals, evaluation, compliance, synthetic data, knowledge graphs, and agentic workflows.

## Getting Started (Low-Cost, No Local Install)

This course uses **Google Gemini's pay-as-you-go API**. A genuine no-card free tier still exists in most regions, including the US — but this course has everyone enable billing anyway, everywhere, because billed ("Paid tier") usage gets Google's stronger data-handling terms (skips human review, isn't used for training), not because Google requires it outside the EEA, UK, and Switzerland, where billing genuinely is mandatory. Usage on the lightweight models this course uses runs at low, pay-as-you-go rates (fractions of a cent per request is typical, but confirm current pricing before you start — Google changes it). Gemini isn't available in mainland China or Hong Kong.

### Quick Start (10 minutes)

1. **Fork this repository**:
   Click "Fork" at the top right of this page. This gives you your own copy at `github.com/YOUR_USERNAME/AI4TM` to save your work into as you go, without touching the original.

2. **Get a Gemini API key**:
   Go to [aistudio.google.com/apikey](https://aistudio.google.com/apikey), enable billing when prompted, and create a key

3. **Open notebooks in Google Colab**:
   Click any `.ipynb` file in this repository → Look for "Open in Colab" badge → Click it

4. **Start with the setup guide**:
   [week_2/lesson08_setup_guide.ipynb](week_2/lesson08_setup_guide.ipynb) — it walks through all of the above in order, plus how to save your work into your fork

**That's it!** No local installation, no complex setup — just a Google account with billing enabled.

### What You Get

- Google Colab - Run code in your browser, no installation
- Gemini API - low pay-as-you-go cost on the lightweight models this course uses (billing must be enabled)
- GitHub - Save and share your work
- Free GPUs in Colab (a separate Colab feature — unaffected by the Gemini API billing change above)

### Privacy Note

Unpaid/free-quota AI usage (Google, OpenAI, etc.) may be reviewed by humans or used to improve models. Google's terms say billed ("Paid tier") Gemini usage is not used for training and skips human review for that purpose — check the "Paid tier" badge in AI Studio to confirm which applies to your key, don't assume. Either way: **only use public, synthetic, or anonymized data in this course.** Never send confidential or client data.

## Course Structure

### Week 2: Essential Concepts
**Topics**: Neural networks, attention, tokenization, embeddings
**Approach**: Production failure modes (light theory)
**Content**:
- [Setup Guide (Notebook)](week_2/lesson08_setup_guide.ipynb) - Colab + Gemini API + GitHub
- [Token Cost Guide (Notebook)](week_2/lesson09_token_cost_guide.ipynb) - Estimate cost before running a batch job

### Week 3: Evaluation
**Topics**: Regression, classification, semantic search
**Content**:
- [Evaluation Template (Notebook)](week_3/lesson12_evaluation_template.ipynb) - Accuracy, precision, recall, F1, confusion matrix
- [Human-in-the-Loop Validation (Notebook)](week_3/lesson13_human_in_the_loop.ipynb) - BLEU, ROUGE, LLM-as-judge, and deciding where a person needs to check the model's work
- [Office Hours: Loading a CSV / Google Sheet and Running evaluate() (Notebook)](week_3/office_hours_load_csv_and_evaluate.ipynb) - Loading a topic-labeled Search Console export from your computer or a Google Sheet, having Gemini assign its own topics, and scoring them with the evaluation template

### Week 4: Compliance
**Topics**: AI compliance and regulatory considerations
**Content**:
- **What is the EU AI Act, and Why You Should Care** - Risk categories, provider vs. deployer, the 2026 Digital Omnibus timeline, GDPR overlap (Circle platform)
- **Reviewing Your Own Architecture for Compliance** - A reusable six-step worksheet applying the AI Act criteria to any system you build (Circle platform)
- **Explore a Real-World Use Case** - A real enterprise case study (Starbucks EMEA, built at Monks) read against the AI Act criteria (Circle platform)
- [Setting Up and Protecting Your API Keys (Notebook)](week_4/lesson18_api_key_security.ipynb) - Setup and protection guidelines, keeping keys out of GitHub and out of AI chat prompts
- [Protecting PII When You Use AI (Notebook)](week_4/lesson17_pii_protection.ipynb) - What counts as PII, redacting it before it reaches a prompt, scrubbing a dataframe before an API call
- [Finding Risk Points in an AI Pipeline (Notebook)](week_4/lesson16_pipeline_risk_points.ipynb) - Applying DLP principles across a full pipeline, spot-the-vulnerability exercise

### Week 5: Synthetic Data
**Topics**: Generating and using synthetic data for marketing
**Content**:
- [Synthetic Data Pipeline (Notebook)](week_5/synthetic_data_pipeline.ipynb) - Preprocessing a table, training and tuning a synthetic data generator, and evaluating the synthetic output against the original

### Week 6: Knowledge Graphs
**Topics**: Nodes, edges, and Cypher; turning a set of documents into a graph with an LLM and merging the duplicates it produces; what a graph answers that a table struggles with; GraphRAG and checking whether an answer is actually grounded in the graph
**Content**:
- [Setup: your knowledge graph environment (Notebook)](week_6/setup_guide.ipynb) - Neo4j AuraDB Free signup, connecting the graph database, and a swappable `LLM_PROVIDER` config so the rest of the week's notebook can switch model providers by changing one value
- [Building and querying a knowledge graph (Notebook)](week_6/knowledge_graph_pipeline.ipynb) - Extracting entities and relationships from a set of internal documents, merging duplicate entities, loading and querying in Cypher, and GraphRAG with a groundedness check

### Week 7: Agentic Workflows
**Topics**: Search intent taxonomies, clustering a search performance export into content gaps, an agent (tools + a loop) that reads that table, generating a landing page brief and evaluating it against the Week 3 template
**Content**:
- [Building an agentic content pipeline (Notebook)](week_7/agentic_content_pipeline.ipynb) - Rebuilding a compact content-gap table, then a hand-written tool-calling loop (three read-only tools, two visible stopping conditions) that turns it into grounded content recommendations
- [Generating and evaluating a landing page brief (Notebook)](week_7/landing_page_brief_generator.ipynb) - A guardrailed brief generator for one content gap, scored by reusing Week 3's evaluation template against a mix of LLM-judged and objectively-recomputed criteria

##  Tools Used

- **Google Colab** (default) - Cloud-based notebooks, no installation
- **Google Gemini API** (default, low-cost pay-as-you-go, billing required) - AI model access
- **GitHub** - Version control and portfolio

**Already have OpenAI or Anthropic API?** You can use those instead — see the optional section in the setup notebook.

## For Instructors

- All notebooks designed for Google Colab (one-click from GitHub)
- Local setup available as optional/advanced path
- Students work in their own fork, never as collaborators on this repository — nobody but the instructor team can push to it, forking or not. `main` is branch-protected (PR review required, no force-push or deletion).

##  For Students

### Before Each Week
1. Open that week's notebook in Colab
2. Make sure your API key is in Secrets (🔑 icon)
3. Run the setup cells

### Tips
- **Save often**: File → Save a copy in GitHub, into your fork
- **Experiment**: Try changing code to see what happens
- **Watch your spend**: this course runs on billed usage, not the free tier — check pricing at [AI Studio](https://aistudio.google.com/apikey) and use the token cost guide before a big batch job
- **No real data**: Only use public or made-up data

##  Important Notes

- **Never commit API keys** - use Colab Secrets or `.env` files (local). See [week_4/lesson18_api_key_security.ipynb](week_4/lesson18_api_key_security.ipynb) for how keys leak and how to catch it.
- This course has you enable billing on your Google account everywhere, even though a genuine no-card free tier still exists in most regions — billing is only Google-*required* in the EEA, UK, and Switzerland; elsewhere it's this course's own choice, for the data-handling benefit below
- Data-use policy (human review, model training) depends on whether your key is on a "Paid tier" project — check the badge in AI Studio, don't assume

## Optional: Local Setup

For experienced users who prefer local development, see the "Optional B: Local Setup" section in [week_2/lesson08_setup_guide.ipynb](week_2/lesson08_setup_guide.ipynb).

Most learners should use Google Colab (the default path).

##  Questions?

Bring them to the office hours or use your course space to post them :)

---

**Ready to learn AI for Marketing? Start here:** [Week 2 Setup Guide](week_2/lesson08_setup_guide.ipynb)
