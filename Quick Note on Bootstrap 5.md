# Note on Bootstrap 5

✍🏽Bootstrap 5 is a well-known front-end framework that provides a collection of CSS and JavaScript components for building responsive and modern web pages. It offers a wide range of pre-designed elements and utilities, making it easier to create consistent and visually appealing layouts. Here are some key features and examples of Bootstrap 5:

1. Responsive Grid System:
Bootstrap 5 includes a responsive grid system that allows you to create flexible and responsive layouts. It uses a 12-column grid system that can be easily customized to suit your needs. Here's an example of a grid layout:
    
    ```
    <div class="container">
      <div class="row">
        <div class="col-md-6">Column 1</div>
        <div class="col-md-6">Column 2</div>
      </div>
    </div>
    
    ```
    
2. Typography:
Bootstrap 5 provides typography classes for easy and consistent text styling. You can apply classes like `h1`, `lead`, `text-muted`, etc., to format your text. Here's an example:
    
    ```
    <h1 class="display-4">Heading</h1>
    <p class="lead">A catchy subheading.</p>
    <p class="text-muted">Some additional text in a muted color.</p>
    
    ```
    
3. Buttons:
Bootstrap 5 offers various button styles and sizes. You can use classes like `btn`, `btn-primary`, `btn-lg`, etc., to create buttons. Here's an example:
    
    ```
    <button class="btn btn-primary">Primary Button</button>
    <button class="btn btn-secondary">Secondary Button</button>
    
    ```
    
4. Navbar:
Bootstrap 5 provides a responsive navigation bar component that automatically collapses on smaller screens. Here's an example:
    
    ```
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <a class="navbar-brand" href="#">Logo</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
        aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">About</a>
          </li>
        </ul>
      </div>
    </nav>
    
    ```
    
5. Cards:
Bootstrap 5 provides a flexible card component for displaying content. Cards can include headers, images, buttons, etc. Here's an example:
    
    ```
    <div class="card" style="width: 18rem;">
      <img src="image.jpg" class="card-img-top" alt="Image">
      <div class="card-body">
        <h5 class="card-title">Card Title</h5>
        <p class="card-text">Some text to describe the card.</p>
        <a href="#" class="btn btn-primary">Learn More</a>
      </div>
    </div>
    
    ```