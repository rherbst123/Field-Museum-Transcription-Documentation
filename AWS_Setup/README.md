# AWS CLI and BOTO3 Setup
-  This is a setup for AWS CLI, the LLM provider for Transcriber-CLI

## Installation Instructions

### Windows

1. Download the AWS CLI MSI installer from the official AWS website:
    - [AWS CLI Installer for Windows](https://awscli.amazonaws.com/AWSCLIV2.msi)

2. Run the downloaded MSI installer and follow the on-screen instructions.

3. Verify the installation by opening Command Prompt or PowerShell and running:
    ```powershell
    aws --version
    ```

**Alternative: Using winget**
```powershell
winget install Amazon.AWSCLI
```

### Linux

**Ubuntu/Debian:**
```bash
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```

**Using apt (older version):**
```bash
sudo apt update
sudo apt install awscli
```

**Verify installation:**
```bash
aws --version
```

### Post-Installation Configuration

After installing AWS CLI, configure your credentials:

```bash
aws configure
```

You will be prompted to enter:
- AWS Access Key ID
- AWS Secret Access Key
- Default region name (e.g., `us-east-1`)
- Default output format (e.g., `json`)