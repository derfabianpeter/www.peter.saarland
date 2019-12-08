brew install hugo || brew upgrade hugo
hugo new site peter-web
git init
git submodule add https://github.com/shenoybr/hugo-goa themes/goa
echo 'theme = "goa"' >> config.toml
hugo new about.md
hugo new kontakt.md
