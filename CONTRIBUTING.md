# Contributing & Personal Workflow

This repository is primarily a personal learning workspace for the 5-Day AI Agents Intensive course. The guidelines below serve two purposes:
1.  **As a personal checklist** to maintain organization and security.
2.  **For any external contributors** who wish to suggest improvements.

---

## 🚨 CRITICAL: Security Rules

This is the most important rule. **Never commit secrets.**

### NEVER Commit:

* API keys or tokens (e.g., `GOOGLE_API_KEY`)
* `.env` files or environment configuration files
* `kaggle.json` credentials
* Any file containing personal passwords or secrets

### Always:

* **Use Kaggle Secrets** for API keys when working in Kaggle notebooks.
* **Use `.env` files** (which are gitignored) for storing local API keys.
* **Review your changes** with `git diff --cached` *before* you commit to ensure no secrets are staged.
* **Review your history** with `git log -p` if you suspect you may have accidentally committed a secret in the past.

---

## 📓 Personal Development Workflow

This is the standard process for adding course materials to the repo.

### 1. Adding Daily Notebooks & Notes

1.  **Complete** the day's notebook on the Kaggle course platform.
2.  **Download** the notebook (`File > Download .ipynb`).
3.  **Save** the notebook to the correct folder (e.g., `dayN_*/`).
4.  **Update** the `notes.md` file in the same folder with your key takeaways, insights, or questions.
5.  **Commit** your changes using the best practices below.

### 2. Git Best Practices

* **Atomic Commits:** Make small, focused commits that represent a single logical change. This makes your history easy to read and understand.

    ```bash
    # Good: Separate commits for separate changes
    git add day1_intro_to_agents/agent_basics.ipynb
    git commit -m "Add Day 1 notebook: Agent basics"

    git add day1_intro_to_agents/notes.md
    git commit -m "Update Day 1 notes: Key takeaways"
    ```

* **Commit Frequency:**
    * Commit **after completing each day's notebook**.
    * Commit **when adding significant notes or insights**.
    * Commit **before making experimental changes** (you can always squash them later).

* **Clear Commit Messages:** Write concise and descriptive messages.
    * `Add Day 1 notebook: Agent basics`
    * `Update Day 2 notes: Multi-agent patterns`
    * `Fix typo in README`
    * `Add resources: Gemini API documentation`

---

## 📁 Repository Structure

### Daily Folders

Each day's folder should contain the core learning materials:
dayN_topic_name/ ├── main_notebook.ipynb # Downloaded from Kaggle └── notes.md # Personal takeaways and insights


### Resources Folder

All reference materials, links, and guides live here:

resources/ ├── course_links.md # Official course URLs └── kaggle_notes.md # Setup guides, API tips, etc.


---

## 💡 How to Contribute (For External Users)

If you have forked this repo and would like to suggest an improvement (e.g., a new resource, a typo fix, or a clarification in the notes):

1.  **Fork the repository.**
2.  **Create a feature branch:** `git checkout -b feature/your-improvement`
3.  **Make your changes** and test them if applicable.
4.  **Submit a pull request** with a clear description of what you changed and why.

---

## ❓ Questions or Issues?

* **For course-specific help:** Check the [Kaggle Discord](https://kaggle.com/discord/confirmation).
* **For official documentation:** Review `resources/course_links.md`.
* **For repo-specific issues:** Open a GitHub issue.

---

## 📜 License

All content in this repository, including contributions, is licensed under the MIT License. See [LICENSE](LICENSE) for details.