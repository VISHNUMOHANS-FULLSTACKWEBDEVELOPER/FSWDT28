# FSWDT28
day28
html
<!DOCTYPE html>
<html>
    <head>
        <title>Js build Project</title>
          <!-- Font awesome icons -->
    <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css"
    integrity="sha512-KfkfwYDsLkIlwQp6LFnl8zNdLGxu9YAA1QvwINks4PhcElQSvqcyVLLD9aMhXd13uQjoXtEKNosOWaZqXgel0g=="
    crossorigin="anonymous"
    referrerpolicy="no-referrer"
  />
        <!-- styles -->
        <link href="./index.css" rel="stylesheet"/>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">

    </head>
    <body>
<!-- Small Screen size buton -->
      <div class="add__new__button__only d-md-none ">
       <button class="btn btn-outline-primary align items-center gap-3" type="submit"data-bs-toggle="modal" data-bs-target="#addModal">
        <i class="fa-solid fa-plus mr-4 "></i> Add new item
       </button>
      </div>
<!-- open task model -->
<div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog modal-lg">
    <div class="modal-content">
      <div class="modal-header">
        <h1 class="modal-title fs-5" id="exampleModalLabel">Task Details...</h1>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body task__modal__body">
        ...
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
        <!-- <button type="button" class="btn btn-primary">Save changes</button> -->
      </div>
    </div>
  </div>
</div>

<!-- Modal -->
      <div class="modal fade" id="addModal" tabindex="-1" aria-labelledby="addModalLabel" aria-hidden="true">
  <div class="modal-dialog modal-dialog-centered">
    <div class="modal-content">
      <div class="modal-header">
        <h1 class="modal-title fs-5" id="addModal">Add New Task</h1>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        <form>
          <!-- img -->
          <div class="mb-3">
            <label for="Imgurl" class="form-label">Image Url</label>
            <input type="email" class="form-control" id="Imgurl" aria-describedby="ImgDesc" placeholder="https://vishnumohan/img">
            <div id="ImgDesc" class="form-text" >This is an optional field for you</div>
          </div>
          <!-- title -->
          <div class="mb-3">
            <label for="Tilte" class="form-label">Task Title</label>
            <input type="email" class="form-control" id="Imgurl" aria-describedby="TitleDesc" placeholder="TaskTitle">
          </div>
          <!-- Task type -->
          <div class="mb-3">
            <label for="Task Type" class="form-label">Task Type</label>
            <input type="tag" class="form-control" id="Tasktype" aria-describedby="TasktypeDesc" placeholder="TaskType">
          </div>
        <!-- Task Description -->
         <div>
          <label for="Text description" class="form-label">Text description</label>
          <textarea
             type="text" class="form-control" id="Textdescription"  placeholder="Text Description" rows="3" required
          ></textarea>
        </div>
        </form>
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
        <button type="submit" class="btn btn-primary">Save changes</button>
      </div>
    </div>
  </div>
      </div>
<!-- Nav Bar -->
        <nav class="navbar navbar-expand-lg bg-body-tertiary">
            <div class="container-fluid">
              <a class="navbar-brand" href="#">Js project</a>
              <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
              </button>
              <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                  <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li class="nav-item">
                      <a class="nav-link active" aria-current="page" href="#">Home</a>
                    </li>
                    </ul>
                </div>
                      <button class="btn btn-outline-primary align items-center gap-3" type="submit"data-bs-toggle="modal" data-bs-target="#addModal">
                        <i class="fa-solid fa-plus mr-4 "></i> Add new item
                  </button>
              </div>
            </div>
          </nav>
          <div class="container">
            <section class="mt-4">
              <div class="row justify content-center">
                <div class=".col-md-6">
                   <div class="input-group flex-nowrap shadow-lg rounded">
                    <input type="search"class="form-control" placeholder="Search your ask here"aria-label="Search task" aria-describedby="addon-wrapping"
                    <span class="input-group-text" id="addon-wrapping">
                      <i class="fas fa-search m-2"></i>
                    </span>
                  </div>
                </div>
               <!-- <div class=".col-md-6">
                  
                </div> -->
              </div>
            </section>
            <section class="mt-4">
              <!-- cards -->
               <div class="row task__contents"></div>
            </section>
          </div>







<!-- Scripts -->
        <script src="./index.js"></script>
        <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
        <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.8/dist/umd/popper.min.js" integrity="sha384-I7E8VVD/ismYTF4hNIPjVp/Zjvgyol6VFvRkX/vR+Vc4jQkC+hVqc2pM8ODewa9r" crossorigin="anonymous"></script>
        <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.min.js" integrity="sha384-0pUGZvbkm6XF6gxjEnlmuGrJXVbNuzT9qBBavbLwCsOGabYfZo0T0to5eqruptLy" crossorigin="anonymous"></script>

    </body>
</html>
js
// var state={
//     taskdetails:[
//         {
//         imgUrl:"",
//         taskdetails:"",
//         tasktype:"",
//         taskdescription:"",
//         },
//         {
//          imgUrl:"",
//          taskdetails:"",
//          tasktype:"",
//          taskdescription:"",
//         },
//         {
//          imgUrl:"",
//          taskdetails:"",
//          tasktype:"",
//          taskdescription:"",
//          },
//         {
//         imgUrl:"",
//         taskdetails:"",
//         tasktype:"",
//         taskdescription:"",
//         },
//     ],
// };
const state={
    taskdetails:[]
};
// DOM operations
const taskcontents= document.querySelector(".task__contents");
const taskmodal= document.querySelector(".task__modal__body");
// console.log(taskcontents);
// console.log(taskmodal);
