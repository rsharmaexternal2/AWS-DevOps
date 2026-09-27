# AWS-DevOps
AWS-Test

===Terraform ===

# 1. Define the desired version (Change to whichever version you need)
TERRAFORM_VERSION="1.11.0"

# 2. Download the zip file (Adjust "linux_amd64" to "darwin_amd64" for Mac, or "windows_amd64" for Windows)
curl -LO "https://releases.hashicorp.com/terraform/1.11.0/terraform_1.11.0_linux_amd64.zip"

# 3. Unzip the package
unzip terraform_1.11.0_linux_amd64.zip

# 4. Move the executable to a directory included in your system $PATH
sudo mv terraform /usr/local/bin/

# 5. Clean up the downloaded file
rm terraform_1.11.0_linux_amd64.zip

==========

# 1. Update your system packaging tool and install required utilities
sudo apt-get update && sudo apt-get install -y gnupg software-properties-common curl

# 2. Download and install the official HashiCorp GPG key
curl -fSsL https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg

# 3. Add the official HashiCorp repository to your system
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://hashicorp.com(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list

# 4. Update the package lists and install Terraform
sudo apt-get update && sudo apt-get install -y terraform
