# navbar

```css
nav {
    background-color: rgba(0,0,0,.65);
    position: absolute;
    top:0;
    left:0;
    padding: 50px 0 0 0;
    width: 100%;
}
nav::after{
    content: "";
    clear:both;
    display:block;
}

nav ul{
    list-style: none;
    margin: 0;
    padding: 0;
}
nav ul li:hover{
    background-color: #2b0306;
}

nav ul li:hover > ul{
    display:block;
}
nav ul li a{
    display: inline-block;
    color:#fff;
    padding: 10px 20px;
    width: 125px;
    text-decoration: none;
    position: relative;
}

nav ul li a:visited {
    color: #fff;
}

nav ul li a:hover {
    background-color: #6d0911;
}

nav ul ul {
    position: absolute;
    top:100%;
    background-color: #2b0306;
    display: none;
}
nav ul ul li{
    position: relative;
}
nav ul ul ul {
    left: 100%;
    top:0;
}
/* top level */

nav > ul{
    padding-left:200px;
}

nav > ul > li {
    float:left;
}

nav > ul > li > a {
    width: auto;
    padding: 10px 20px 15px 20px;
}
```

```html
<nav>
				<ul>
					<li>
						<a title="About us" href = "#">About us</a>
						<ul>
							<li><a title="Sublink 1" href = "#">Sublink 1</a></li>
							<li><a title="Sublink 2" href = "#">Sublink 2</a></li>

						</ul>
					</li>
					<li>
						<a title="Design corner" href = "#">Design corner</a>
						<ul>
								<li><a title="Sublink 1" href = "#">Sublink 1</a></li>
								<li><a title="Sublink 2" href = "#">Sublink 2</a></li>
								<li><a title="Sublink 3" href = "#">Sublink 3</a>
									<ul>
										<li><a title="Sub Sublink 1" href = "#">Sublink 1</a></li>
										<li><a title="Sub Sublink 2" href = "#">Sublink 2</a></li>
									</ul>
								</li>
	
						</ul>
					</li>
					<li>
						<a title="Design corner" href = "#">Products</a>
						<ul>
								<li><a title="Sublink 1" href = "#">Sublink 1</a></li>
								<li><a title="Sublink 2" href = "#">Sublink 2</a></li>
	
						</ul>
					</li>
					<li>
						<a title="Design corner" href = "#">Contact Us</a>
						<ul>
								<li><a title="Sublink 1" href = "#">Sublink 1</a></li>
								<li><a title="Sublink 2" href = "#">Sublink 2</a></li>
	
						</ul>
					</li>
				</ul>
			</nav>
```

**Note:**

For android: top levels link have to have `#` . Else the browser will navigate away.

For windows tablet: top levels link have to have `aria-haspopup="true"` else css hover won't be triggered.