<!DOCTYPE html>

<html lang="en">

    <head>

        <meta charset="utf-8">
        <meta name="viewport" content="initial-scale=1, width=device-width">

        <!-- http://getbootstrap.com/docs/5.1/ -->
        <link crossorigin="anonymous" href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" rel="stylesheet">
        <script crossorigin="anonymous" src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p"></script>

        <link href="/static/styles.css" rel="stylesheet">

        <title>FrogWatch {% block title %}{% endblock %}</title>

    </head>

    <body>
        <nav class="border navbar navbar-expand-md" style=background-color:#47592B;>
            <div class="container-fluid">
                <a class="navbar-brand" href="/"><span class="green">Frog</span><span class="white">Watch</span><span class="tan"> USA</span></a>
                <button aria-controls="navbar" aria-expanded="false" aria-label="Toggle navigation" class="navbar-toggler" data-bs-target="#navbar" data-bs-toggle="collapse" type="button" style=color:#FB5F44>
                    MENU
                </button>
                <div class="collapse navbar-collapse" id="navbar">
                    {% if session["user_id"] %}
                        <ul class="navbar-nav me-auto mt-2">
                            <li class="nav-item"><a class="nav-link" href="/protocols">Monitoring Protocols</a></li>
                            <li class="nav-item"><a class="nav-link" href="/surverysitereg">Survery Site Registration</a></li>
                            <li class="nav-item"><a class="nav-link" href="/logwatches">Log Watches</a></li>
                            <li class="nav-item"><a class="nav-link" href="/profile">Profile</a></li>
                        </ul>
                        <ul class="navbar-nav ms-auto mt-2">
                            <li class="nav-item"><a class="nav-link" href="/logout">Log Out</a></li>
                        </ul>
                    {% else %}
                        <ul class="navbar-nav ms-auto mt-2">
                            <li class="nav-item"><a class="nav-link" href="/register">Register</a></li>
                            <li class="nav-item"><a class="nav-link" href="/login">Log In</a></li>
                            <li class="nav-item"><a class="nav-link" href="/homepage">Homepage</a></li>
                        </ul>
                    {% endif %}
                </div>
            </div>
        </nav>

        {% if get_flashed_messages() %}
            <header>
                <div class="alert alert-primary mb-0 text-center" role="alert">
                    {{ get_flashed_messages() | join(" ") }}
                </div>
            </header>
        {% endif %}

        <main class="container-fluid py-5">
            {% block main %}{% endblock %}
        </main>

    </body>

</html>





## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/alliesoldau/recycledcontentpercentages/edit/main/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/alliesoldau/recycledcontentpercentages/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
