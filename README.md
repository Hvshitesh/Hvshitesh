<h1 align="center">Hi <img src="https://raw.githubusercontent.com/benbahrenburg/benbahrenburg/main/assets/wave.gif" width="40" alt="Boy's in Jacket">, I'm Hitesh</h1>
<h3 align="center">A passionate Python Developer from India</h3><br>
<img align="center" src="https://devtechnosys.com/insights/wp-content/uploads/2022/02/MEAN-Stack-Work.gif" alt="Boy's in Jacket"><br>
<h1>Tech Stack ⚒️</h1>

[![GitHub Streak](https://streak-stats.demolab.com/?user=Hvshitesh&theme=tokyonight-duo)](https://git.io/streak-stats)
<br><br>
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=Hvshitesh&layout=compact&theme=tokyonight)](https://github.com/anuraghazra/github-readme-stats)
<br><br>
![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=Hvshitesh&show_icons=true&theme=tokyonight)


- uses: Platane/snk@v2
  with:
    # github user name to read the contribution graph from (**required**)
    # using action context var `github.repository_owner` or specified user
    github_user_name: ${{ github.repository_owner }}

    # list of files to generate.
    # one file per line. Each output can be customized with options as query string.
    #
    #  supported options:
    #  - palette:     A preset of color, one of [github, github-dark, github-light]
    #  - color_snake: Color of the snake
    #  - color_dots:  Coma separated list of dots color.
    #                 The first one is 0 contribution, then it goes from the low contribution to the highest.
    #                 Exactly 5 colors are expected.
    outputs: |
      dist/github-snake.svg
      dist/github-snake-dark.svg?palette=github-dark
      dist/ocean.gif?color_snake=orange&color_dots=#bfd6f6,#8dbdff,#64a1f4,#4b91f1,#3c7dd9
      
      
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="github-snake.svg" />
  <img alt="github-snake" src="github-snake.svg" />
</picture>

