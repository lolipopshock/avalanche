# Avalanche Blog Template for Jekyll 

Avalanche is a highly configurable research portfolio website template based [Jekyll](https://jekyllrb.com) and [bulma](https://bulma.io).

## Installation

1. Install Jekyll via their [official instructions](https://jekyllrb.com/docs/installation/). 

2. Download this repository, install dependencies, and start the server

    ```bash
    git clone https://github.com/lolipopshock/avalanche.git && cd avalanche
    bundle install
    bundle exec jekyll serve
    ```

## Get started and publish to Github Pages 

- Please check the [tutorial](https://lolipopshock.github.io/avalanche/2021/09/03/Starter.html).

## Highly configurable templates

Besides website titles and URLs, we provide a list of configurations for customizing your website in the `_data` folder. This includes: 

1. Regular website settings `_config.yml`:

    ```yaml
    title: Your Name
    description: >
        The portfolio website for you.
    baseurl: "" 
    url: "" 
    ```

2. Configure texts on the index page `_data/meta.yml`: 

    ```yaml
    index:
        welcome_message:
        personal_photo:
        news_highlight_color:
        personal_description:
    ```
3. And update the news using `_data/news.csv` file. 

4. Add your social media accounts by editing `social` in `_data*/settings.yml`: 

5. Change tabs on your website `_data/settings.yml`:

    ```yaml
    menu:
        - {name: 'About', file: ''}
        - {name: 'Research', file: 'research.html'}
        - {name: 'Blog', file: 'blog.html'}
    ```

6. Customize the publication page (see in the next section):


## Auto generated publication page

Believing your publication page is not simply a repetition of your google scholar page, we design the publication page that helps you organize your work and present them to the audience in a clean and intuitive fashion. 

The publication page is rendered based on the `_data/settings.csv` table. Explanation for the features in the table: 
 - `type`: The type of the publication, e.g., workshop paper, conference paper, journal paper. Defined in the `_data/meta.yml` file. 
 - `topic`: The shorthand for the *topic* of the publication. Topics are defined in the `_data/settings.yml` file. 
 - `name`: A shorthand name for the paper. 
 - `author`: Authors of the paper. You could use markdown grammar like `**` to bold your names. 
 - `title`: The title of the paper. 
 - `venue`, `publisher`: The venue of a conference paper, or the publisher of a journal paper. 
 - `paper`, `website`, `arxiv`, `poster`, `video`: The links to the paper's pdf, project website, arxiv page, poster, or video.
 - `img`: An overview image for the paper. You could use the `/assets/publications/placeholder.png` if you don't have the images. 

We provide a tab in the research page, which helps you group your publications by specific categories. By doing so, you need to: 
1. Set the categories' display names `name` and shorthand names `id` in the `_data/settings.yml` file. For example: 
    ```yaml
    publication: 
        topics:
        - {name: 'All',            id: 'all',  description: ''} # it will automatically handle the `all` category
        - {name: 'Deep Learning',  id: 'dl',   description: ''}
        - {name: 'GAN',            id: 'gan',  description: ''}
        - {name: 'Other',          id: 'misc', description: ''}
    ```
2. For each paper, set their category in the `topic` feature using the corresponding `id` for the category.

You can also consider group papers based on their `type`s.
