<!DOCTYPE html>
<html>

<head>
    <!--Import Google Icon Font-->
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"
        integrity="sha256-/xUj+3OJU5yExlq6GSYGSHk7tPXikynS7ogEvDej/m4=" crossorigin="anonymous"></script>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/js/materialize.min.js"></script>


    <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
    <!--Import materialize.css-->
    <!-- Compiled and minified CSS -->

    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/css/materialize.min.css">


    <!--Let browser know website is optimized for mobile-->
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
</head>

<body>


    <nav>
        <!-- navbar content here  -->
    </nav>

    <ul id="slide-out" class="sidenav">
        <li>
            <div class="user-view">
                <div class="background">
                    <img
                        src="https://images.pexels.com/photos/12043242/pexels-photo-12043242.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1">
                </div>

                <a href="#name"><span class="white-text name">John Doe</span></a>
                <a href="#email"><span class="white-text email">jdandturk@gmail.com</span></a>
            </div>
        </li>
        <li>
            <a href="#!"><i class="material-icons">cloud</i>Create Polls

            </a></li>
        <li><a href="#!"><i class="material-icons">ac_unit</i> See Answers</a></li>


        <li>
            <div class="divider"></div>
        </li>
        <li><a class="subheader">Account</a></li>
        <li><a class="waves-effect" href="#!"> <i class="material-icons">account_circle</i> Logout</a></li>
    </ul>
    <a href="#" data-target="slide-out" class="sidenav-trigger"><i class="material-icons">menu</i></a>


    <div class="row container">
        <form class="col s12">
            <div class="row">
                <div class="input-field col s12">
                    <input placeholder="Placeholder" id="first_name" type="text" class="validate">
                    <label for="first_name">First Name</label>
                </div>
            </div>
            <div class="col-lg-12">
                <div id="row">
                    <div class="input-group m-3">
                        <div class="input-group-prepend">

                        </div>
                        <input type="text" class="form-control m-input">
                    </div>
                </div>

                <div id="newinput"></div>
                <button id="rowAdder" type="button" class="btn btn-dark">
                    <span class="bi bi-plus-square-dotted">
                    </span> ADD
                </button>

                <button class="btn btn-primary" id="DeleteRow" type="button">
                    <i class="bi bi-trash"></i>
                    Delete
                </button>
            </div>


        </form>
    </div>



    <script>
        (function ($) {
            $(function () {

                $('.sidenav').sidenav();
                $('.parallax').parallax();

            }); // end of document ready
        })(jQuery);


        $("#rowAdder").click(function () {
            newRowAdd =
                '<div id="row"> <div class="input-group m-3">' +
                '<div class="input-group-prepend">' +
                '<button class="btn btn-primary" id="DeleteRow" type="button">' +
                '<i class="bi bi-trash"></i>  Delete</button> </div>' +
                '<input type="text" class="form-control m-input"> </div> </div>';

            $('#newinput').append(newRowAdd);
        });

        $("body").on("click", "#DeleteRow", function () {
            $(this).parents("#row").remove();
        })
    </script>


</body>

</html>
