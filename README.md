# PaperPusher
## 📄 Research Article Auto-Pusher Bot (Web UI)

This is a simple tool designed to automatically search for the latest, most relevant research articles and push them to a Slack channel. It uses the Europe PMC API for searching and the Slack Incoming Webhook service for message delivery.

### 🚀 Project Demo

You can access and use the live web version of this tool here:

**[https://yu-1011.github.io/PaperPusher/PaperRadar_en.html](https://yu-1011.github.io/PaperPusher/PaperRadar_en.html)**

### ✨ Core Features

* **Keyword & Journal Filtering:** Precisely target articles using custom keywords and a list of target journals/preprints (e.g., `Nature`, `bioRxiv`).
* **Strict AND Logic:** Keywords are combined using **AND** logic, ensuring that the retrieved articles contain all set keywords, which greatly improves relevance.
* **Timeframe Selection:** Supports searching by publication date within the "Last 7 Days," "Last 30 Days," or "Last 1 Year" to ensure content freshness.
* **Slack Integration:** Formats the list of found articles into a clean Slack message (including title, authors, source, and direct link) for one-click pushing to a specified Slack channel.
* **Client-Side Execution:** As a pure front-end HTML/JavaScript application, your Webhook URL, search configurations, and logs are processed entirely within your browser and are not transmitted to any external server (other than the official Slack and Europe PMC APIs).

### 🛠️ How to Configure and Run

Using this tool is straightforward. You only need to configure three key pieces of information:

#### 1. Get Your Slack Webhook URL

This is the critical component for sending messages to Slack.

* Go to your Slack workspace.
* Search for and add the **"Incoming Webhooks"** app.
* Configure the Webhook, selecting the channel where you want to receive notifications.
* Copy the generated **Webhook URL** and paste it into the **"Slack Webhook URL"** field on the web interface.

#### 2. Configure Keywords and Sources

* **Custom Keywords (Keywords):** Enter the keywords for the research areas you follow, separated by commas `,`.
    * *Example:* `Genomics, single cell, cancer`
    * *Logic:* The search results will contain `Genomics` **AND** `single cell` **AND** `cancer`.
* **Custom Journal List (Journals / Preprints):** Enter the names of the journals or preprint servers you trust or follow, separated by commas `,`.
    * *Example:* `Nature, Science, Cell, bioRxiv`

#### 3. Run the Pusher

* Select your desired **Search Timeframe** and **Max Results Per Page**.
* Click the **"Run Auto-Pusher"** button.
* The tool will execute the Europe PMC search. Once complete, the results will be pushed to your Slack channel and displayed in the log area at the bottom of the page.

### ⚙️ Technical Details

* **Data Source:** [Europe PMC RESTful API](https://europepmc.org/RestfulWebService).
* **Front-End Technology:** HTML, JavaScript, [Tailwind CSS](https://tailwindcss.com/).
* **Author:** Yu Chen ([github@yu-1011](https://github.com/yu-1011))
