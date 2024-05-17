# Scanner Notebooks

This repository contains a collection of Jupyter Notebooks crafted by the Scanner team designed specifically for security use cases. These notebooks are designed for practical, real-world use cases and are intended to help security professionals efficiently analyze and respond to security incidents using common log sources.

## Features
- Comprehensive Examples: Explore a wide range of security use cases, including investigating unusual API activity, detecting privilege escalation attempts, monitoring resource deletion or termination events, identifying compromised user credentials, and analyzing data exfiltration attempts.
- Common Log Sources: The notebooks cover analysis for various security log source types, such as AWS CloudTrail and Cloudflare HTTP logs, providing the necessary tools to perform thorough investigations and gain valuable insights.
- Interactive Analysis: Leverage the power of Jupyter Notebooks for interactive data exploration and visualization, enabling security teams to quickly identify and respond to potential threats.

## Getting Started
The fastest way to get started is to install the **JupyterLab Desktop** app locally on your computer, and install the Scanner Python SDK into your Jupyter notebook.

### Step 1: Download JupyterLab Desktop
Simply download and run the appropriate installer for your OS. You can find [download links on the Github page here](https://github.com/jupyterlab/jupyterlab-desktop?tab=readme-ov-file#installation).

### Step 2: Open this repository to view notebooks
Launch the **JupyterLab Desktop** app, and open this repository. You can open these notebooks and run them.

### Step 3: Import and configure the Scanner API Client
In your Jupyter notebook, run this command to import the Scanner API client:

```
from scanner_client import Scanner
```
In the Scanner UI, visit Settings and copy-paste your API URL and API key. We recommend adding them to environment variables like `SCANNER_API_URL` and `SCANNER_API_KEY`. 

Once that is done, you can create the Scanner API client in your Jupyter notebook:

```
scanner = Scanner(
    api_url=os.environ["SCANNER_API_URL"],
    api_key=os.environ["SCANNER_API_KEY"],
)
```
You are now ready to execute queries and perform investigations.

## FAQs

### After running `%pip install` on a visualization library, the visualization is not appearing.

Sometimes, after you install a library that renders a visualization in a Jupyter cell, the visualization won't appear until after you reboot the Jupyter session. This is because the library needs to install an extension into JupyterLab.

In **JupyterLab Desktop**, you can close the session by clicking the hamburger menu button in the top right. When you open a new session, the visualization should now work.


## Contributing
We welcome contributions from the community! If you have an idea for a new use case or improvements to existing notebooks, please open an issue or submit a pull request. Your feedback and contributions help make this repository better for everyone.

## License
This repository is licensed under the Apache 2.0 License. See the LICENSE file for more details.