# SSH Key Generation and Setup (Optional but Recommended)

# Step 1: Generate a New SSH Key (replace "you@example.com" with your email address)
ssh-keygen -t rsa -b 4096 -C "you@example.com"

# Step 2: Start the SSH Agent
eval "$(ssh-agent -s)"

# Step 3: Add Your SSH Key to the Agent
ssh-add ~/.ssh/id_rsa

# Step 4: Copy the SSH Key to Your Clipboard
cat ~/.ssh/id_rsa.pub

# Step 5: Add SSH Key to GitHub
# 1. Go to your GitHub account settings.
# 2. Click on SSH and GPG keys.
# 3. Click New SSH key, paste the copied key, and save.

# Step 6: Clone a Repository Using SSH
git clone git@github.com:username/repo.git
