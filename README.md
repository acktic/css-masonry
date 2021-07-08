# css-masonry
Create a masonry view of multiple elements

# use

`document.querySelector('.container').classList.add('flexbox')`<br>
`document.querySelectorAll('.item').forEach((a) => a.classList.add('flexbox'))`<br>

# note

Container must be taller than the tallest column, how I did it...

`    var height = 0;`<br>
`    var second = 0;`<br>
`    var groups = 0;`<br>
`    var column = document.querySelectorAll('.item:nth-child(3n+1)');`<br>
`    for (i = 0; i < column.length - 1; i++) height += column[i].clientHeight;`<br>
`    var column = document.querySelectorAll('.item:nth-child(3n+2)');`<br>
`    for (i = 0; i < column.length - 1; i++) second += column[i].clientHeight;`<br>
`    var column = document.querySelectorAll('.item:nth-child(3n+3)');`<br>
`    for (i = 0; i < column.length - 1; i++) groups += column[i].clientHeight;`<br>
`    var max = Math.max(height, second, groups);`<br>
`    document.querySelector('.container').style.height =`<br>
`      '${(max + 1000).toString()}px'`<br>


# link

https://tobiasahlin.com/blog/masonry-with-css/
