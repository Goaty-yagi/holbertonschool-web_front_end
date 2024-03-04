# Learning Objectives

- [Which guidelines to follow for HTML](#Which-guidelines-to-follow-for-HTML)
- [How to create the skeleton of an HTML5 page](#How-to-create-the-skeleton-of-an-HTML5-page)
- [How to use semantic HTML tags to structure a web page](#How-to-use-semantic-HTML-tags-to-structure-a-web-page)
- [Which use cases to use div vs span](#Which-use-cases-to-use-div-vs-span)
- [The semantic value’s of header, main, footer, article, nav, section, aside](#The-semantic-value’s-of-header,-main,-footer,-article,-nav,-section,-aside)
- [How to use headings (and why it’s important to follow the hierarchical order)](<#How-to-use-headings-(and-why-it’s-important-to-follow-the-hierarchical-order)>)
- [How to make lists in HTML](#How-to-make-lists-in-HTML)
- [The differences between medias (SVG, GIF, PNG, JPG)](#The-differences-between-medias "SVG, GIF, PNG, JPG")
- [How to structure data in a table](#How-to-structure-data-in-a-table)
- [How to integrate a video in a webpage](#How-to-integrate-a-video-in-a-webpage)
- [How to integrate an audio file in a webpage](#How-to-integrate-an-audio-file-in-a-webpage)
- [How to embed external content](#How-to-embed-external-content)
- [How to correctly structure an HTML page](#How-to-correctly-structure-an-HTML-page)

## Which guidelines to follow for HTML

### Use Semantic HTML:

- Use appropriate HTML tags to represent the structure and meaning of your content (e.g., <header>, <nav>, <section>, <article>, <footer>).
- Avoid using non-semantic tags like <div> or <span> when more specific semantic tags are available.

## How to create the skeleton of an HTML5 page

To create the basic skeleton of an HTML5 page, you need to include essential elements such as <!DOCTYPE html>, <html>, <head>, <meta>, <title>, and <body>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Your Page Title</title>
    <!-- Additional head elements, such as stylesheets or scripts, can go here -->
  </head>
  <body>
    <!-- Your page content goes here -->
  </body>
</html>
```

## How to use semantic HTML tags to structure a web page

- <header> is used for the header section, which typically includes the main heading and navigation.
- <nav> is used for navigation links.
- <main> contains the main content of the page, including <section> for grouping related content.
- <article> is used for individual articles or posts within a <section>.
- <aside> is used for content related to the main content, such as a sidebar.
- <footer> is used for the footer section, which often includes copyright information and additional links.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Your Page Title</title>
    <!-- Additional head elements, such as stylesheets or scripts, can go here -->
  </head>
  <body>
    <header>
      <!-- Header content, e.g., logo, navigation, etc. -->
      <h1>Main Heading or Site Name</h1>
      <nav>
        <!-- Navigation links go here -->
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
      </nav>
    </header>

    <main>
      <section>
        <!-- Main content sections -->
        <article>
          <!-- Individual articles or posts -->
          <h2>Article Title</h2>
          <p>Article content goes here.</p>
        </article>

        <article>
          <h2>Another Article Title</h2>
          <p>More content for another article.</p>
        </article>
      </section>

      <aside>
        <!-- Sidebar or additional content -->
        <h2>Related Links</h2>
        <ul>
          <li><a href="#">Link 1</a></li>
          <li><a href="#">Link 2</a></li>
          <li><a href="#">Link 3</a></li>
        </ul>
      </aside>
    </main>

    <footer>
      <!-- Footer content, e.g., copyright, links, etc. -->
      <p>&copy; 2024 Your Website Name. All rights reserved.</p>
    </footer>
  </body>
</html>
```

## Which use cases to use div vs span

- div: block level contents
- span: inlinr contents

## The semantic value’s of header, main, footer, article, nav, section, aside

### <header>:

- Semantic Value:
  Represents the introductory content of a section or a page.
- Use Case:
  Typically used to contain heading elements (<h1> - <h6>), logos, navigation, and other header-related content.

### <main>:

- Semantic Value:
  Represents the main content of a document or application.
- Use Case:
  Contains the primary content of a webpage, excluding headers, footers, and sidebars.

### <footer>:

- Semantic Value:
  Represents the footer of a section or a page.
- Use Case:
  Contains metadata, copyright information, links to related documents, or other footer-related content.

### <article>:

- Semantic Value:
  Represents a self-contained piece of content that could be distrib uted and reused independently, such as a news article, blog post, or forum post.
- Use Case:
  Wraps content that can be treated as an independent unit and can be syndicated or shared.

### <nav>:

- Semantic Value:
  Represents a navigation menu.
- Use Case:
  Used to contain links for navigation purposes, such as site navigation menus or menus within a specific section.

### <section>:

- Semantic Value:
  Represents a thematic grouping of content, typically with a heading.
- Use Case:
  Divides content into meaningful sections, helping to organize and structure the document.

### <aside>:

- Semantic Value:
  Represents content that is tangentially related to the content around it, often presented as a sidebar.
- Use Case:
  Contains information such as related links, advertisements, or additional content that is related but not the main focus.

## How to use headings (and why it’s important to follow the hierarchical order)

### Why it's important to follow the hierarchical order:

- Semantic Structure: Headings provide a semantic structure to your content, making it more understandable for both users and search engines.<br>
  They convey the hierarchy and relationships between different sections of your content.

- Accessibility: Screen readers and other assistive technologies use heading tags to provide users with an overview of the page's structure.<br>
  Proper heading order ensures that users can navigate through the content in a logical and meaningful way.

- SEO (Search Engine Optimization): Search engines use heading tags to understand the content hierarchy and importance.
  Using proper heading order can positively impact search engine rankings, as search engines interpret well-structured content as more relevant and authoritative.

- Styling and Consistency: Following a hierarchical order helps maintain consistency in styling. CSS styles are often applied based on heading levels.
  Consistent styling improves the visual appearance and readability of the page.

- Document Outline: HTML headings contribute to the document outline. When users view the document outline in browsers or when using certain browser extensions, they see the hierarchical structure of the content.

### How to use headings:

- Start with <h1>: Begin with the highest level heading (<h1>) for the main title or heading of the page. This represents the most important information.

- Use Heading Levels Sequentially: Follow with lower-level headings (<h2>, <h3>, etc.) to represent subsections within the main content.
  Avoid skipping heading levels; maintain a logical progression.

- Keep it Concise: Each section should have a clear and concise heading that summarizes the content within that section.

- Avoid Styling for Presentation: Avoid using heading tags solely for styling purposes. Headings should reflect the structure and hierarchy of your content, not just its visual appearance.

## How to make lists in HTML

### Unordered List (<ul>):

An unordered list is used when the order of the items doesn't matter. Bullets or other symbols typically denote the items.

```html
<ul>
  <li>Apples</li>
  <li>Bananas</li>
  <li>Oranges</li>
</ul>
```

### Ordered List (<ol>):

An ordered list is used when the order of the items matters. Numbers or letters are typically used to denote the order.

```html
<ol>
  <li>Define the goal</li>
  <li>Plan the approach</li>
  <li>Execute the plan</li>
  <li>Evaluate the results</li>
</ol>
```

### Description List (<dl>):

A description list is used to group terms with their corresponding descriptions.

```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>

  <dt>CSS</dt>
  <dd>Cascading Style Sheets</dd>

  <dt>JS</dt>
  <dd>JavaScript</dd>
</dl>
```

## The differences between medias (SVG, GIF, PNG, JPG)

- Use SVG for vector graphics and logos that need to scale without loss of quality.
- Use GIF for simple animations or graphics with a limited color palette.
- Use PNG for images with transparency or when lossless compression is crucial.
- Use JPG for photographs and images with complex color gradients where some loss of quality is acceptable.

## How to structure data in a table

- <table> element is used to define the table.
- <thead> is used for the table header, and <tr> represents a table row within the header.
- <th> is used for table header cells, providing bold and centered text by default.
- <tbody> is used for the table body, and <tr> represents each row within the body.
- <td> is used for table data cells.

```html
<table border="1">
  <thead>
    <tr>
      <th>ID</th>
      <th>Name</th>
      <th>Position</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>John Doe</td>
      <td>Software Engineer</td>
      <td>$80,000</td>
    </tr>
    <tr>
      <td>2</td>
      <td>Jane Smith</td>
      <td>UX Designer</td>
      <td>$75,000</td>
    </tr>
    <!-- Add more rows as needed -->
  </tbody>
</table>
```

## How to integrate a video in a webpage

```html
<video width="640" height="360" controls poster="poster.jpg">
  <source src="example.mp4" type="video/mp4" />
  Your browser does not support the video tag.
</video>
```

- The <video> element is used to embed the video.
- The width and height attributes set the dimensions of the video player.
- The controls attribute adds play, pause, and volume controls to the video player.
- The <source> element inside the <video> element specifies the video file (example.mp4) and its type (video/mp4).

It's important to include alternative text or content between the opening and closing <video> tags. This content will be displayed if the browser does not support the <video> element or if the specified video format is not supported.

## How to integrate an audio file in a webpage

<audio controls poster="audio-poster.jpg">
    <source src="example.mp3" type="audio/mp3">
    Your browser does not support the audio tag.
</audio>

## How to embed external content

```html
<iframe
  src="https://www.example.com"
  width="600"
  height="400"
  frameborder="0"
  allowfullscreen
></iframe>
```

## How to correctly structure an HTML page

Follow all above info and save it with the extension .html
