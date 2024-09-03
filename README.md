# ado-secret-viewer

A tool for securely viewing Azure DevOps Variable Group secrets. This pipeline retrieves variables from a specified group, storing them as artifacts. It allows authorized users to inspect secret values safely, aiding in auditing and troubleshooting Variable Group configurations without compromising security.

## Table of Contents
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Setup](#setup)
- [Usage](#usage)
- [Security Considerations](#security-considerations)
- [Contributing](#contributing)
- [Contact](#contact)

## Features
- Securely retrieves variables from Azure DevOps Variable Groups
- Stores sensitive information as pipeline artifacts
- Enables controlled access to secret values for authorized users
- Facilitates auditing and troubleshooting of Variable Group configurations

## Prerequisites
- Azure DevOps account with appropriate permissions
- Access to the target Variable Group
- Basic understanding of Azure DevOps pipelines

## Setup
1. Clone this repository to your Azure DevOps project.
2. Update the `YOUR_VARIABLE_GROUP_NAME` in the YAML file with your actual Variable Group name.
3. Ensure that the necessary permissions are set for accessing the Variable Group and running the pipeline.

## Usage
1. Navigate to the pipeline in your Azure DevOps project.
2. Run the pipeline manually (as it's set to manual trigger).
3. Once completed, access the pipeline artifacts to view the extracted secrets.

## Security Considerations
- Ensure that access to the pipeline and its artifacts is properly restricted.
- Remember that the secrets are stored in plain text in the artifact. Handle with care.
- Regularly rotate secrets and update the Variable Group accordingly.
- Consider implementing additional encryption for enhanced security.

## Contributing
Contributions to improve ado-secret-viewer are welcome. Please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature.
3. Commit your changes.
4. Push to your branch.
5. Create a new Pull Request.

## Contact

Have questions or suggestions? Reach out to us:
- 📧 Email: [Sauravsrivastav2205@gmail.com](mailto:Sauravsrivastav2205@gmail.com)
- 💼 LinkedIn: [in/sauravsrivastav2205](https://www.linkedin.com/in/sauravsrivastav2205)
- 🐙 GitHub: [https://github.com/SauravSrivastav](https://github.com/SauravSrivastav)
