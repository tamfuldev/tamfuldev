### Hi there 👋

<a href="https://github.com/TranNgocTam-19211TT2494/TranNgocTam-19211TT2494">
    <img src="https://komarev.com/ghpvc/?username=TranNgocTam-19211TT2494&color=blueviolet&style=plastic">
</a>

This is the place where I opensource stuff and break things 🤣


- 🔭 I’m currently working on something cool 😉
- 🌱 I’m currently learning ReatJs , VueJs , Wordpress 
- 💬 Ask me about anything related to HTML/CSS/JAVASCRIP OR Laravel
- ⚡ Fun fact: I ❤️ 🐶s
- 📫 How to reach me: ngoctam2303001@ or https://join.skype.com/invite/yqQVkkDvnlOr

name: GitHub-Profile-Summary-Cards

on:
  schedule: # execute every 24 hours
    - cron: "* */24 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    name: generate-github-profile-summary-cards

    steps:
      - uses: actions/checkout@v2
      - uses: vn7n24fzkq/github-profile-summary-cards@release
        env: # default use ${{ secrets.GITHUB_TOKEN }}, you should replace with your personal access token
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          USERNAME: ${{ github.repository_owner }}


