---
editor_options: 
  markdown: 
    wrap: sentence
---

# Group lab exercise 🏆

------------------------------------------------------------------------

## Group Details

### Group Member 1

-   Name: Aqilah Rafidi
-   Student ID: 22B2149
-   Favourite book: Tomie by Junji Ito
-   Favourite number: 14
-   Favourite mathematical equation: **$a^2+b^2=c^2$**
-   Insert an inspiring photo: ![kiki](https://github.com/sm2302-aug23/.github/assets/141397360/4c2cbf81-5623-40a6-a209-2e14d4266f5c)

### Group Member 2

-   Name: Izznie Adanan
-   Student ID: 22B2125
-   Favourite book: Reel by Kennedy Ryan
-   Favourite number: 22
-   Favourite mathematical equation: **$tan\theta= \frac{sin\theta}{cos\theta}$**
-   Insert an inspiring photo:![Cillian Murphy as Oppenheimer](https://github.com/sm2302-aug23/.github/assets/141397633/7ffa24b9-620f-47ec-891d-3fb2351d645d)

### Group Member 3

-   Name: Syafiqah Raddin
-   Student ID: 22b2046
-   Favourite book: Ikigai
-   Favourite number: 213
-   Favourite mathematical equation: **$x = \frac {-b \pm \sqrt{b^2 -4ac}} {2a}$**
-   Insert an inspiring photo: ![Money](https://github.com/sm2302-aug23/.github/assets/141397169/e96a94c1-02af-4476-a55e-676ff342db0f)

### Group Member 4

-   Name: Bibi Junaidi
-   Student ID: 22B9014
-   Favourite book: Atomic Habit / Crying in H Mart
-   Favourite number: 810
-   Favourite mathematical equation: **$y=mx + c$**
-   Insert an inspiring photo: ![Inspiring_Photo](https://github.com/sm2302-aug23/.github/assets/141397273/f5b5a10c-b6db-40ef-80c9-f280481c796f)

## Collaborative Work

#### ggsave()

1.  Description: `ggsave()` is a convenient function for saving a plot.
    It defaults to saving the last plot that you displayed, using the size of the current graphics device.
    It also guesses the type of graphics device from the extension.

2.  Usage:

```         
ggsave(
  filename,
  plot = last_plot(),
  device = NULL,
  path = NULL,
  scale = 1,
  width = NA,
  height = NA,
  units = c("in", "cm", "mm", "px"),
  dpi = 300,
  limitsize = TRUE,
  bg = NULL,
  ...
)
```

3.  Details: Note: Filenames with page numbers can be generated by including a C integer format expression, such as ⁠%03d⁠ (as in the default file name for most R graphics devices, see e.g. png()).
    Thus, filename = "figure%03d.png" will produce successive filenames figure001.png, figure002.png, figure003.png, etc.
    To write a filename containing the ⁠%⁠ sign, use %%.
    For example, filename = "figure-100%%.png" will produce the filename ⁠figure-100%.png⁠.

4.  Examples

```         
if (FALSE) {
ggplot(mtcars, aes(mpg, wt)) +
  geom_point()

ggsave("mtcars.pdf")
ggsave("mtcars.png")

ggsave("mtcars.pdf", width = 4, height = 4)
ggsave("mtcars.pdf", width = 20, height = 20, units = "cm")

# delete files with base::unlink()
unlink("mtcars.pdf")
unlink("mtcars.png")

# specify device when saving to a file with unknown extension
# (for example a server supplied temporary file)
file <- tempfile()
ggsave(file, device = "pdf")
unlink(file)

# save plot to file without using ggsave
p <-
  ggplot(mtcars, aes(mpg, wt)) +
  geom_point()
png("mtcars.png")
print(p)
dev.off()

}
```

##### Use of arguments width and height in ggsave()

- The arguments width and height are used to resize a plot or an image to a desired size, so using ggsave() can save it as the new resized version.



