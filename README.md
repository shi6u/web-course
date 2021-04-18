<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/css/materialize.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.12.0-2/css/all.min.css"
        integrity="sha256-46r060N2LrChLLb5zowXQ72/iKKNiw/lAmygmHExk/o=" crossorigin="anonymous" />
    <link rel="stylesheet" href="blog.css">
    <link rel="stylesheet" href="BlogsApp.html">
    <title>BlogApp Login</title>
</head>

<body>
    <div class="container login-container">
        <div class="card">
            <div class="card-content">
                <h3><i class="fas fa-blog"></i> BlogApp</h3>
<div class="section">
    <p class="lead">Create blogs</p>
</div>
<div class="divider"></div>
<div class="section">
    <a href="/auth/google" class="btn red darken-1">
        <i class="fab fa-google left"></i> Log In With Google
    </a>
</div>
            </div>
        </div>
    </div>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/js/materialize.min.js"></script>
</body>

</html>

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/css/materialize.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.12.0-2/css/all.min.css"
        integrity="sha256-46r060N2LrChLLb5zowXQ72/iKKNiw/lAmygmHExk/o=" crossorigin="anonymous" />
    <link rel="stylesheet" href="blog.css">
    <link rel="stylesheet" href="blog1app.html">
    <title>BlogsApp</title>
</head>

<body>
    <nav class="grey darken-3">
        <div class="nav-wrapper container">
    
            <a href="#!" class="brand-logo center">BlogsApp</a>
            <a href="#" data-target="mobile-demo" class="sidenav-trigger show-on-large"><i class="fas fa-bars"></i></a>
            <ul class="sidenav" id="mobile-demo">
                <li><a href="/blogs">Public Blogs</a></li>
                <li><a href="/dashboard">Dashboard</a></li>
                <li><a href="/auth/logout">Logout</a></li>
            </ul>
        </div>
    </nav>    <div class="fixed-action-btn">
        <a href="/blogs/add" class="btn-floating btn-large waves-effect waves-light red"><i class="fas fa-plus"></i></a>
    </div>    <div class="container">
        <h1>Dashboard</h1>
<h3>Welcome sarah</h3>
<p>Here are your blogs</p>
<p>You have not created any blogs</p>
    </div>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/js/materialize.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/ckeditor/4.14.1/ckeditor.js"
        integrity="sha256-bEIQpI72w9NJuIVhTLFUF2/8uxl0u5800r8ddViuv+o=" crossorigin="anonymous"></script>

    <script>
        M.Sidenav.init(document.querySelector('.sidenav'))
        M.FormSelect.init(document.querySelector('#status'))

        CKEDITOR.replace('body', {
            plugins: 'wysiwygarea, toolbar, basicstyles, link'
        })
    </script>
</body>

</html>



<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/css/materialize.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.12.0-2/css/all.min.css"
        integrity="sha256-46r060N2LrChLLb5zowXQ72/iKKNiw/lAmygmHExk/o=" crossorigin="anonymous" />
    <link rel="stylesheet" href="blog.css">
    <title>BlogsApp</title>
</head>

<body>
    <nav class="grey darken-3">
        <div class="nav-wrapper container">
    
            <a href="#!" class="brand-logo center">BlogsApp</a>
            <a href="#" data-target="mobile-demo" class="sidenav-trigger show-on-large"><i class="fas fa-bars"></i></a>
            <ul class="sidenav" id="mobile-demo">
                <li><a href="/blogs">Public Blogs</a></li>
                <li><a href="/dashboard">Dashboard</a></li>
                <li><a href="/auth/logout">Logout</a></li>
            </ul>
        </div>
    </nav>    <div class="fixed-action-btn">
        <a href="/blogs/add" class="btn-floating btn-large waves-effect waves-light red"><i class="fas fa-plus"></i></a>
    </div>    <div class="container">
        <h3>Add Blog</h3>
<div class="row">
    <form action="/blogs" method="POST" class="col s12">
        <div class="row">
            <div class="input-field">
                <input type="text" id="title" name="title">
                <label for="title">Title</label>
            </div>
        </div>
        <div class="row">
            <div class="input-field">
                <input type="text" id="image" name="image">
                <label for="image">Image of your blog</label>
            </div>
        </div>

        <div class="row">
            <div class="input-field">
                <select id="status" name="status">
                    <option value="public" selected>Public</option>
                    <option value="private">Private</option>
                </select>
                <label for="status">Status</label>
            </div>
        </div>

        <div class="row">
            <div class="input-field">
                <h5>Blog content:</h5>
                <textarea id="body" name="body"></textarea>
            </div>
        </div>

        <div class="row">
            <input type="submit" value="Save" class="btn">
            <a href="/dashboard" class="btn orange">Cancel</a>
        </div>
    </form>
</div>
    </div>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/js/materialize.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/ckeditor/4.14.1/ckeditor.js"
        integrity="sha256-bEIQpI72w9NJuIVhTLFUF2/8uxl0u5800r8ddViuv+o=" crossorigin="anonymous"></script>

    <script>
        M.Sidenav.init(document.querySelector('.sidenav'))
        M.FormSelect.init(document.querySelector('#status'))

        CKEDITOR.replace('body', {
            plugins: 'wysiwygarea, toolbar, basicstyles, link'
        })
    </script>
</body>

</html>




body{
    background-color: rgb(20, 20, 20);
  }
  p {
    margin: 10px 0 !important;
    color: #fff;
    font-family: cursive;
    
  }
  
  .login-container {
    width: 400px;
    margin-top: 50px;
    text-align: center;
  
  }
  
  .fa-small {
    font-size: 16px !important;
    
  }
  
  .btn-float {
    float: left;
    margin-right: 10px;
    
  }
  
  .img-small {
    width: 180px;
  }
  .card{
    background-color: rgb(0, 41, 46);
  }
  h1{
    color: white;
    font-weight: bolder;
  }
  h3{
    color: yellow;
    font-weight: bold;
  }
  h5{
    color: yellow;
    font-weight: bold;
  }
  
  span{
    color: gray;
  }
  .sidenav {
    background-color: rgb(20, 20, 20);
  }
  .sidenav li a{
    color: #fff;
  }
  th{
    color: gray;
  }
  tbody *{
    color: #fff;
  }
  .input-field *{
    color: #fff;
  }
  #status{
    color: #fff;
  }
