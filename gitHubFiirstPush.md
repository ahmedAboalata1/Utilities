# Step 1: Generate a New SSH Key
# Replace "you@example.com" with your email address to create the SSH key.
ssh-keygen -t rsa -b 4096 -C "you@example.com"

# Step 2: Start the SSH Agent
# This command starts the SSH agent in the background.
eval "$(ssh-agent -s)"

# Step 3: Add Your SSH Key to the Agent
# Adds the newly generated SSH private key to the SSH agent.
ssh-add ~/.ssh/id_rsa

# Step 4: Copy the SSH Key to Your Clipboard
# Displays your SSH public key so you can copy it.
cat ~/.ssh/id_rsa.pub

# Step 5: Add SSH Key to GitHub
# 1. Go to GitHub, and navigate to your account settings.
# 2. Click on "SSH and GPG keys".
# 3. Click "New SSH key", paste the copied key into the key field, and save.

# Step 6: Clone a Repository Using SSH
# Use the SSH URL to clone your repository. Replace "username" and "repo" with your GitHub username and the repository name.
git clone git@github.com:username/repo.git
