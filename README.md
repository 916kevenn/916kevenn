<h1 align="center">Hi 👋, I'm Kevenn Chiguti</h1>
<h3 align="center">A student from UniCesumar(Software Engineer)</h3>

- 🌱 I’m currently learning **Python**

- 📫 How to reach me **kevennks23@gmail.com**

<h3 align="left">Connect with me:</h3>
<p align="left">
<a href="https://linkedin.com/in/kevenn chiguti" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="kevenn chiguti" height="30" width="40" /></a>
</p>

<h3 align="left">Languages and Tools:</h3>
<p align="left"> <a href="https://www.linux.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="linux" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> </p>

<p><img align="left" src="https://github-readme-stats.vercel.app/api/top-langs?username=916kevenn&show_icons=true&locale=en&layout=compact" alt="916kevenn" /></p>

<p>&nbsp;<img align="center" src="https://github-readme-stats.vercel.app/api?username=916kevenn&show_icons=true&locale=en" alt="916kevenn" /></p>

<p><img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=916kevenn&" alt="916kevenn" /></p>



name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: <seu-usuario>
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
