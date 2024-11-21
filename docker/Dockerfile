FROM gitpod/workspace-full:latest

# Install dependencies
RUN apt-get update && apt-get install -y \
    wget \
    unzip \
    && rm -rf /var/lib/apt/lists/*

# Download and install Terraform
RUN wget https://releases.hashicorp.com/terraform/1.0.11/terraform_1.0.11_linux_amd64.zip \
    && unzip terraform_1.0.11_linux_amd64.zip \
    && mv terraform /usr/local/bin/ \
    && rm terraform_1.0.11_linux_amd64.zip

# Install dependencies
RUN apt-get update && apt-get install -y \
    curl \
    apt-transport-https \
    lsb-release \
    gnupg \
    && rm -rf /var/lib/apt/lists/*

# Install Azure CLI
RUN curl -sL https://aka.ms/InstallAzureCLIDeb | bash

RUN pip install -r requirements.txt