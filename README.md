<h1 align="center">Hi <img src="https://raw.githubusercontent.com/benbahrenburg/benbahrenburg/main/assets/wave.gif" width="40" alt="Boy's in Jacket">, I'm Hitesh</h1>
<h3 align="center">A passionate Python Developer from India</h3><br>
<img align="center" src="https://devtechnosys.com/insights/wp-content/uploads/2022/02/MEAN-Stack-Work.gif" alt="Boy's in Jacket"><br>
<h1>Tech Stack ⚒️</h1>

[![GitHub Streak](https://streak-stats.demolab.com/?user=Hvshitesh&theme=tokyonight-duo)](https://git.io/streak-stats)
<br><br>
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=Hvshitesh&layout=compact&theme=tokyonight)](https://github.com/anuraghazra/github-readme-stats)
<br><br>
![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=Hvshitesh&show_icons=true&theme=tokyonight)


# GitHub Action for generating a contribution graph with a snake eating your contributions.

name: Generate Snake

# Controls when the action will run. This action runs every 6 hours.

on:
  schedule:
      # every 6 hours
    - cron: "0 */6 * * *"

# This command allows us to run the Action automatically from the Actions tab.
  workflow_dispatch:

# The sequence of runs in this workflow:
jobs:
  # This workflow contains a single job called "build"
  build:
    # The type of runner that the job will run on
    runs-on: ubuntu-latest

    # Steps represent a sequence of tasks that will be executed as part of the job
    steps:

    # Checks repo under $GITHUB_WORKSHOP, so your job can access it
      - uses: actions/checkout@v2

    # Generates the snake  
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: Hvshitesh
          # these next 2 lines generate the files on a branch called "output". This keeps the main branch from cluttering up.
          gif_out_path: dist/github-contribution-grid-snake.gif
          svg_out_path: dist/github-contribution-grid-snake.svg

     # show the status of the build. Makes it easier for debugging (if there's any issues).
      - run: git status

      # Push the changes
      - name: Push changes
        uses: ad-m/github-push-action@master
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          branch: master
          force: true

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          # the output branch we mentioned above
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

