<!DOCTYPE html>
<html>

<head>
    <link rel="stylesheet" href="assets/css/font-awesome/css/font-awesome.min.css">
    <link rel="stylesheet" href="assets/css/style.css">
    <link rel="stylesheet" href="assets/plugins/datatables-bs4/css/dataTables.bootstrap4.min.css">
    <link rel="stylesheet" href="assets/plugins/datatables-responsive/css/responsive.bootstrap4.min.css">
    <link rel="stylesheet" href="assets/plugins/datatables-buttons/css/buttons.bootstrap4.min.css">
</head>

<body>
    <div class="main">
        <div style="justify-content: space-around;">
            <div class="div1">
                <div class="div2">
                    <i class="fa fa-home fa-plus"></i>
                    <a href="#">New User</a>
                </div>
                <div class="div3">
                    <input type="checkbox" id="result">
                    <a>Hide Disabled User</a>
                </div>
            </div>
            <section class="content">
                <div class="container-fluid">
                    <div class="row">
                        <div class="col-12">
                            <div class="card">
                                <!-- /.card-header -->
                                <div class="card-body">
                                    <table id="example1" class="table table-bordered table-striped">
                                        <thead>
                                            <tr>
                                                <th>ID</th>
                                                <th>User Name</th>
                                                <th>Email</th>
                                                <th>Enabled</th>
                                            </tr>
                                        </thead>
                                        <tbody>
                                            <tr>
                                                <td>1</td>
                                                <td>AdminUser</td>
                                                <td>admin@piworks.net</td>
                                                <td>True</td>
                                            </tr>
                                            <tr id="enabled">
                                                <td>2</td>
                                                <td>Test User</td>
                                                <td>testuser@piworks.net</td>
                                                <td>False</td>
                                            </tr>
                                        </tbody>
                                    </table>
                                </div>
                                <!-- /.card-body -->
                            </div>
                            <!-- /.col -->
                        </div>
                        <!-- /.row -->
                    </div>
                    <!-- /.container-fluid -->
                </div>
            </section>
        </div>
        <div style="margin-left: auto; width:100%;">
            <form>
                <div class="div1" style="justify-content: space-around;">
                    <div class="div4" style="margin-left: auto;">
                        <input type="submit" name="save user" value="Save User">
                    </div>
                </div>
                <div style="margin-left: auto;">
                    <div class="formtitle">
                        <a>New User</a>
                    </div>
                    <div class="pos">
                        <div class="label" style="margin-top:0px !important;">
                            <a>Username:</a>
                        </div>
                        <div class="form2">
                            <input type="text" name="username">
                        </div>
                    </div>
                    <div class="pos">
                        <div class="label">
                            <a>Display Name:</a>
                        </div>
                        <div class="form2">
                            <input type="text" name="displayname">
                        </div>
                    </div>
                    <div class="pos">
                        <div class="label">
                            <a>Phone:</a>
                        </div>
                        <div class="form2">
                            <input type="text" name="phone">
                        </div>
                    </div>
                    <div class="pos">
                        <div class="label">
                            <a>Email:</a>
                        </div>
                        <div class="form2">
                            <input type="text" name="email">
                        </div>
                    </div>
                    <div class="pos">
                        <div class="label">
                            <a>User Roles:</a>
                        </div>
                        <div class="form2">
                            <SELECT type="checkbox" name="roles" style="height:36px; width:308px;">
                                <option value disabled selected>Select user roles...</option>
                                <option>Guest</option>
                                <option>Admin</option>
                                <option>SuperAdmin</option>
                            </SELECT>
                        </div>
                    </div>
                    <div class="pos">
                        <div class="label">
                            <a>Enabled:</a>
                        </div>
                        <div class="form2">
                            <input type="checkbox" name="enabled">
                        </div>
                    </div>
                </div>
            </form>
        </div>
    </div>
    <footer>

    </footer>
    <script src="assets/plugins/jquery/jquery.min.js"></script>
    <script src="assets/plugins/datatables/jquery.dataTables.min.js"></script>
    <script src="assets/plugins/datatables-bs4/js/dataTables.bootstrap4.min.js"></script>
    <script src="assets/plugins/datatables-responsive/js/dataTables.responsive.min.js"></script>
    <script src="assets/plugins/datatables-responsive/js/responsive.bootstrap4.min.js"></script>
    <script src="assets/plugins/datatables-buttons/js/dataTables.buttons.min.js"></script>
    <script src="assets/plugins/datatables-buttons/js/buttons.bootstrap4.min.js"></script>
    <script src="assets/plugins/datatables-buttons/js/buttons.html5.min.js"></script>
    <script src="assets/plugins/datatables-buttons/js/buttons.colVis.min.js"></script>

    <script>

        $(function () {
            $("#example1").DataTable({
                "responsive": true,
                "lengthChange": false,
                "autoWidth": false,
                "info": false,
                "paging": false,
                "searching": false,
            })
        });
    </script>
    <script>
        $(document).ready(function(){
          $("#result").click(function(){
            $("[id='enabled']").toggle();
          });
        });
        </script>
</body>

</html>