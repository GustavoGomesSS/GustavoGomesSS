
- 🌱 Linguagens de maior dominância: Java, JavaScript, C#, Python, Html e css**

- 📫 How to reach me **gomesbraz541@gmail.com**

![snake gif](https://github.com/GustavoGomesSS/GustavoGomesSS/blob/output/github-contribution-grid-snake.svg)

name: "generate-snake-game-from-github-contribution-grid"
description: "Generates a snake game from a github user contributions grid. Output the animation as gif or svg"
author: "platane"

runs:
  using: docker
  image: docker://platane/snk@sha256:3169a2e4a5b5181c203ae18e7075d0d92be88a0cdeabce6c3221288ef6a17675

inputs:
  github_user_name:
    description: "github user name"
    required: true
  outputs:
    required: false
    default: null
    description: |
      list of files to generate.
      one file per line. Each output can be customized with options as query string.
       supported query string options:
      - palette:      A preset of color, one of [github, github-dark, github-light]
      - color_snake:  Color of the snake
      - color_dots:   Coma separated list of dots color. 
                      The first one is 0 contribution, then it goes from the low contribution to the highest.
                      Exactly 5 colors are expected.
      example:
        outputs: |
          dark.svg?palette=github-dark&color_snake=blue
          light.svg?color_snake=#7845ab
          ocean.gif?color_snake=orange&color_dots=#bfd6f6,#8dbdff,#64a1f4,#4b91f1,#3c7dd9
