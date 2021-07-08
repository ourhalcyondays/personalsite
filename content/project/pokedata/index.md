---
date: "2021-06-02T00:00:00Z"
external_link: ""
image:
  caption: 
  focal_point: Smart
  preview: true
  preview_only: false
header:
  image: ""
  caption: ""
links:
- icon: palette
  icon_pack: fas
  name: Portfolio
  url: https://jessicaqiu.myportfolio.com/pokedata
summary: So you’ve caught 'em all. Now what? Now, we plot of course! A Data Visualization Experiment using a Pokémon dataset.
tags:
- R
- Data Visualization
- Pokémon
title: Gotta Catch 'Em All (Pokémon Data Visualization in R)
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""
share: false
---

{{< toc >}}

## 💡 I. Introduction

I have proven what Pokémon nerds have suspected all along:

**Not all Pokémon are created equal.** But exactly how unequal are things in the Pokémon world?

To find out, I compared the three most basic indicators of a Pokémon's strength; attack power, defensive power, and HP (health points). Taking data from [this dataset](https://www.kaggle.com/rounakbanik/pokemon), I broke down Pokémon by their primary types (water, fire, grass and electric). Then, it was time to plot.


The goals of this project were to learn how to create bubble plots in R using base functions and to dip my toes into data visualization!

{{< figure src="Pokedata Cover.png" caption="" >}}

## 📊 II. Pokédata Findings

I decided to make **bubble plots** to compare Pokémon stats. Bubble plots are scatterplots on steroids. They are interesting because they easily convey information on three dimensions. Besides the normal x-axis and y-axis dimensions, they can also represent data through the size of the point, or bubble.

{{< figure src="WaterPokemonBubblePlot2.png" caption="" >}}
{{< figure src="ElectricPokemonBubblePlot2.png" caption="" >}}
{{< figure src="FirePokemonBubblePlot2.png" caption="" >}}
{{< figure src="GrassPokemonBubblePlot2.png" caption="" >}}

View the full project showcase here or at my [portfolio](https://jessicaqiu.myportfolio.com/pokedata)!
{{< figure src="Pokedata.png" caption="" >}}

## 💻 III. Poké R Code 

Interested in viewing the code? Check it out here. To get custom fonts "Bebas" and "Titillium Web" into R, I used the {showtext} & {extrafont} packages.


```
#Import custom fonts
library('extrafont')
font_import()
loadfonts()
fonts() #view available fonts
library(showtext)
font_add("tw", "Titillium Web.ttf")
font_add_google("Titillium Web", "tw")

#Water type ----------------------------------------------------------

png("WaterPokemonBubblePlot2.png", width = 10, height = 7, units = 'in', res = 300)
radius <- sqrt( waterpokemon$hp/ pi )
symbols(waterpokemon$attack, waterpokemon$defense,
        circles = radius, inches = 0.4, fg = "#ffffff00", 
        bg = "#8fd4d740", main = "",
        cex.main = 2.5,
        ylab = "",
        xlab = "",
        col.lab = "#297b90",
        col.axis = "#297b90",
        col.main = "#297b90",
        ylim=c(7,150),
        xlim=c(5,160),
        yaxs="i",
        xaxs="i",
        axes = FALSE,
        family = '',
        )
box(bty="l", col= "#297b90")
axis(2, col.ticks= "#297b90", col= "#297b90", col.axis = "#297b90",
     family ="Bebas")
axis(1, col.ticks= "#297b90", col= "#297b90", col.axis = "#297b90",
     family ="Bebas")

showtext_begin()
text(waterpokemon$attack, waterpokemon$defense, waterpokemon$name,
     col= "#297b90", cex=2, family ="tw", font = 2)
showtext_end()
dev.off()

# Electric type ----------------------------------------------------------

png("ElectricPokemonBubblePlot.png", width = 10, height = 7, units = 'in', res = 300)
radius <- sqrt( electricpokemon$hp/ pi )
symbols(electricpokemon$attack, electricpokemon$defense,
        circles = radius, inches = 0.4, fg = "#ffffff00", 
        bg = "#fde37540", main = "",
        cex.main = 2.5,
        ylab = "",
        xlab = "",
        col.lab = "#f9ca04",
        col.axis = "#f9ca04",
        col.main = "#f9ca04",
        ylim=c(7,125),
        xlim=c(20,130),
        yaxs="i",
        xaxs="i",
        axes = FALSE,
        family = '',
)
box(bty="l", col= "#c89d02")
axis(2, col.ticks= "#c89d02", col= "#c89d02", col.axis = "#c89d02",
     family ="Bebas")
axis(1, col.ticks= "#c89d02", col= "#c89d02", col.axis = "#c89d02",
     family ="Bebas")

showtext_begin()
text(electricpokemon$attack, electricpokemon$defense, electricpokemon$name,
     col= "#c89d02", cex=2, family ="tw", font = 2)
showtext_end()
dev.off()

# Grass type ------------------------------------------------------------

png("GrassPokemonBubblePlot.png", width = 10, height = 7, units = 'in', res = 300)
radius <- sqrt( grasspokemon$hp/ pi )
symbols(grasspokemon$attack, grasspokemon$defense,
        circles = radius, inches = 0.4, fg = "#ffffff00", 
        bg = "#afd16240", main = "",
        cex.main = 2.5,
        ylab = "",
        xlab = "",
        col.lab = "#72a62e",
        col.axis = "#72a62e",
        col.main = "#72a62e",
        ylim=c(20,140),
        xlim=c(20,140),
        yaxs="i",
        xaxs="i",
        axes = FALSE,
        family = '',
)
box(bty="l", col= "#669627")
axis(2, col.ticks= "#669627", col= "#669627", col.axis = "#669627",
     family ="Bebas")
axis(1, col.ticks= "#669627", col= "#669627", col.axis = "#669627",
     family ="Bebas")

showtext_begin()
text(grasspokemon$attack, grasspokemon$defense, grasspokemon$name,
     col= "#669627", cex=2, family ="tw", font = 2)
showtext_end()
dev.off()

# Fire type ------------------------------------------------------------

png("FirePokemonBubblePlot.png", width = 10, height = 7, units = 'in', res = 300)
radius <- sqrt( firepokemon$hp/ pi )
symbols(firepokemon$attack, firepokemon$defense,
        circles = radius, inches = 0.4, fg = "#ffffff00", 
        bg = "#e8886f40", main = "",
        cex.main = 2.5,
        ylab = "",
        xlab = "",
        col.lab = "#72a62e",
        col.axis = "#72a62e",
        col.main = "#72a62e",
        ylim=c(25,150),
        xlim=c(25,135),
        yaxs="i",
        xaxs="i",
        axes = FALSE,
        family = '',
)
box(bty="l", col= "#cc532b")
axis(2, col.ticks= "#cc532b", col= "#cc532b", col.axis = "#cc532b",
     family ="Bebas")
axis(1, col.ticks= "#cc532b", col= "#cc532b", col.axis = "#cc532b",
     family ="Bebas")

showtext_begin()
text(firepokemon$attack, firepokemon$defense, firepokemon$name,
     col= "#cc532b", cex=2, family ="tw", font = 2)
showtext_end()
dev.off()
```

## 💭 IV. Closing Thoughts