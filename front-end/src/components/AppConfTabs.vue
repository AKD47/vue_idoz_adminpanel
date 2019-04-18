<template>
    <div>
        <el-tabs type="border-card">
            <el-tab-pane label="API User">
                <div class="col-lg-12 grid-margin">
                     <div class="card">
                         <div class="card-body d-flex justify-content-center">
                             <el-button icon="el-icon-plus" type="primary" @click="addUserModal()">
                               Create API User
                             </el-button>
                             <!--<el-button type="success" icon="el-icon-plus" @click="addUserModal()" circle></el-button>-->
                         </div>
                     </div>
                </div>
                <data-tables
                        :data="tableApiUsers"
                        :filters="filters"
                        v-loading="loading"
                        width="100%">
                    <el-table-column
                            prop="username"
                            label="User Name"
                            custom
                            width="auto">
                    </el-table-column>
                    <el-table-column
                            prop="actions"
                            label="Actions"
                            width="320">
                        <template slot-scope="props">
                            <!--<button class="btn btn-success ml-2 mr-2" @click="showEditApiUser(props.row.username)">-->
                                <!--Edit-->
                            <!--</button>-->
                            <el-button type="primary" icon="el-icon-edit" @click="showEditApiUser(props.row.username)" circle></el-button>
                            <el-button type="danger" icon="el-icon-delete" circle></el-button>
                            <!--<button type='button' class='btn btn-danger ml-2 mr-2'>-->
                                <!--Delete-->
                            <!--</button>-->
                        </template>
                    </el-table-column>
                </data-tables>
                <!--<el-row class="d-flex flex-wrap justify-content-end" style="margin-bottom: 10px">-->
                        <!--<el-button type="success" icon="el-icon-plus" circle></el-button>-->
                <!--</el-row>-->
            </el-tab-pane>
            <el-tab-pane label="Aux Billing User">
                <div class="col-lg-12 grid-margin">
                    <div class="card">
                        <div class="card-body d-flex justify-content-center">
                            <el-button icon="el-icon-plus" type="primary" @click="addUserModal()">
                                Create Aux Billing User
                            </el-button>
                        </div>
                    </div>
                </div>
                <data-tables
                        :data="tableUsers"
                        :filters="filters"
                        v-loading="loading"
                        width="100%">
                    <el-table-column
                            prop="firstName"
                            label="First Name"
                            custom
                            width="auto">
                    </el-table-column>
                    <el-table-column
                            prop="lastName"
                            label="Last Name"
                            custom
                            width="auto">
                    </el-table-column>
                    <el-table-column
                            prop="country"
                            label="Country"
                            width="auto">
                    </el-table-column>
                    <el-table-column
                            prop="actions"
                            label="Actions"
                            width="320">
                        <template slot-scope="props">
                            <!--<button class="btn btn-success ml-2 mr-2" @click="showEditUserModal(props.row.firstName)">-->
                                <!--Edit-->
                            <!--</button>-->
                            <!--<button type='button' class='btn btn-danger ml-2 mr-2'>-->
                                <!--Delete-->
                            <!--</button>-->
                            <el-button type="primary" icon="el-icon-edit" @click="showEditUserModal(props.row.firstName)" circle></el-button>
                            <el-button type="danger" icon="el-icon-delete" circle></el-button>
                        </template>
                    </el-table-column>
                </data-tables>
            </el-tab-pane>
            <el-tab-pane label="Billing User">
                <div class="col-lg-12 grid-margin">
                    <div class="card">
                        <div class="card-body d-flex justify-content-center">
                            <el-button icon="el-icon-plus" type="primary" @click="addUserModal()">
                                Create Billing User
                            </el-button>
                        </div>
                    </div>
                </div>
                <data-tables
                        :data="tableUsers"
                        :filters="filters"
                        v-loading="loading"
                        width="100%">
                    <el-table-column
                            prop="firstName"
                            label="First Name"
                            custom
                            width="auto">
                    </el-table-column>
                    <el-table-column
                            prop="lastName"
                            label="Last Name"
                            custom
                            width="auto">
                    </el-table-column>
                    <el-table-column
                            prop="country"
                            label="Country"
                            width="auto">
                    </el-table-column>
                    <el-table-column
                            prop="actions"
                            label="Actions"
                            width="320">
                        <template slot-scope="props">
                            <!--<button class="btn btn-success ml-2 mr-2" @click="showEditUserModal(props.row.firstName)">-->
                                <!--Edit-->
                            <!--</button>-->
                            <!--<button type='button' class='btn btn-danger ml-2 mr-2'>-->
                                <!--Delete-->
                            <!--</button>-->
                            <el-button type="primary" icon="el-icon-edit" @click="showEditUserModal(props.row.firstName)" circle></el-button>
                            <el-button type="danger" icon="el-icon-delete" circle></el-button>
                        </template>
                    </el-table-column>
                </data-tables>
            </el-tab-pane>
            <el-tab-pane label="Tech User">
                <div class="col-lg-12 grid-margin">
                    <div class="card">
                        <div class="card-body d-flex justify-content-center">
                            <el-button icon="el-icon-plus" type="primary" @click="addUserModal()">
                                Create Tech User
                            </el-button>
                        </div>
                    </div>
                </div>
                <data-tables
                        :data="tableUsers"
                        :filters="filters"
                        v-loading="loading"
                        width="100%">
                    <el-table-column
                            prop="firstName"
                            label="First Name"
                            custom
                            width="auto">
                    </el-table-column>
                    <el-table-column
                            prop="lastName"
                            label="Last Name"
                            custom
                            width="auto">
                    </el-table-column>
                    <el-table-column
                            prop="country"
                            label="Country"
                            width="auto">
                    </el-table-column>
                    <el-table-column
                            prop="actions"
                            label="Actions"
                            width="320">
                        <template slot-scope="props">
                            <!--<button class="btn btn-success ml-2 mr-2" @click="showEditUserModal(props.row.firstName)">-->
                                <!--Edit-->
                            <!--</button>-->
                            <!--<button type='button' class='btn btn-danger ml-2 mr-2'>-->
                                <!--Delete-->
                            <!--</button>-->
                            <el-button type="primary" icon="el-icon-edit" @click="showEditUserModal(props.row.firstName)" circle></el-button>
                            <el-button type="danger" icon="el-icon-delete" circle></el-button>
                        </template>
                    </el-table-column>
                </data-tables>
            </el-tab-pane>
            <el-tab-pane label="Admin User">
                <div class="col-lg-12 grid-margin">
                    <div class="card">
                        <div class="card-body d-flex justify-content-center">
                            <el-button icon="el-icon-plus" type="primary" @click="addUserModal()">
                                Create Admin User
                            </el-button>
                        </div>
                    </div>
                </div>
                <data-tables
                        :data="tableUsers"
                        :filters="filters"
                        v-loading="loading"
                        width="100%">
                    <el-table-column
                            prop="firstName"
                            label="First Name"
                            custom
                            width="auto">
                    </el-table-column>
                    <el-table-column
                            prop="lastName"
                            label="Last Name"
                            custom
                            width="auto">
                    </el-table-column>
                    <el-table-column
                            prop="country"
                            label="Country"
                            width="auto">
                    </el-table-column>
                    <el-table-column
                            prop="actions"
                            label="Actions"
                            width="320">
                        <template slot-scope="props">
                            <!--<button class="btn btn-success ml-2 mr-2" @click="showEditUserModal(props.row.firstName)">-->
                                <!--Edit-->
                            <!--</button>-->
                            <!--<button type='button' class='btn btn-danger ml-2 mr-2'>-->
                                <!--Delete-->
                            <!--</button>-->
                            <el-button type="primary" icon="el-icon-edit" @click="showEditUserModal(props.row.firstName)" circle></el-button>
                            <el-button type="danger" icon="el-icon-delete" circle></el-button>
                        </template>
                    </el-table-column>
                </data-tables>
            </el-tab-pane>
        </el-tabs>
        <div id="AddUserModal" class="product-modal">
            <div class="product-modal__content">
                <span class="close product-modal__close" id="closeAddUserModal">x</span>
                <div class="modal-body product-modal__body">
                    <div id="AddUserModalResult" class="form-group"></div>
                    <div class="modal-footer product-modal__footer">
                        <button type="submit" class="btn btn-primary" id="submitAddUserModal">Confirm</button>
                    </div>
                </div>
            </div>
        </div>
        <div id="updateApiModal" class="product-modal">
            <div class="product-modal__content">
                <span class="close product-modal__close" id="closeApiModal">x</span>
                <div class="modal-body product-modal__body">
                    <div id="ApiModalResult" class="form-group"></div>
                    <div class="modal-footer product-modal__footer">
                        <button type="submit" class="btn btn-primary" id="submitApiModal">Confirm</button>
                    </div>
                </div>
            </div>
        </div>
        <div id="updateUserModal" class="product-modal">
            <div class="product-modal__content">
                <span class="close product-modal__close" id="closeUserModal">x</span>
                <div class="modal-body product-modal__body">
                   <div id="UserModalResult" class="form-group"></div>
                   <div class="modal-footer product-modal__footer">
                     <button type="submit" class="btn btn-primary" id="submitUserModal">Confirm</button>
                   </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "app-conf-tabs",
        data() {
            return {
                tableApiUsers: [],
                tableUsers: [],
                filters: [
                    {
                        value: '',
                        search_prop: 'name'
                    }
                ],
                total: 0,
                loading: true
            }
        },
        mounted() {
            this.loadApiUser();
            this.loadUsers();
        },
        methods: {
            loadApiUser: function () {
                let datarequest = new XMLHttpRequest();
                datarequest.onreadystatechange = function(v) {
                    if (datarequest.readyState == 4) {
                        v.loading = false;
                        v.tableApiUsers = datarequest.response;
                        // console.log(v.tableApiUsers);
                    }
                }.bind(datarequest, this);//
                datarequest.open('GET', 'http://www.json-generator.com/api/json/get/bVMezbjbfS?indent=2 ');
                datarequest.responseType = 'json';
                datarequest.send();
            },
            loadUsers: function () {
                let datarequest = new XMLHttpRequest();
                datarequest.onreadystatechange = function(v) {
                    if (datarequest.readyState == 4) {
                        v.loading = false;
                        v.tableUsers = datarequest.response;
                        // console.log(v.tableUsers);
                    }
                }.bind(datarequest, this);//
                datarequest.open('GET', 'http://www.json-generator.com/api/json/get/bPTteKElYO?indent=4');
                datarequest.responseType = 'json';
                datarequest.send();
            },
            showEditApiUser: function (edit) {
                let editUser = this.tableApiUsers.find((item) => item.username === edit);
                // let targetUserIndex = this.tableApiUsers.findIndex((item) => item.username === edit);
                let modal = document.getElementById('updateApiModal');
                let close = document.getElementById("closeApiModal");
                let submit = document.getElementById('submitApiModal');
                let result = document.getElementById('ApiModalResult');

                submit.disabled = false;

                result.innerHTML = `<div class="form-group">
                                        <label>User Name</label>
                                        <input type="text" value="${editUser.username}" id="editApiModalUsername" required class="form-control">
                                    </div>
                                    <div class="form-group">
                                        <label>Key</label>
                                        <input type="text" value="${editUser.key}" id="editApiModalKey" required class="form-control">
                                    </div>`;

                modal.classList.remove('modal__close');
                modal.setAttribute("style", "opacity: 1; z-index:9999;");
                close.onclick = function() {
                    modal.setAttribute("style", "opacity: 0; z-index:-1;");
                    result.innerHTML = " ";
                };
                window.onclick = function(event) {
                    if (event.target == modal) {
                        modal.setAttribute("style", "opacity: 0; z-index:-1;");
                        result.innerHTML = " ";
                    }
                };
                submit.onclick = function(v, event) {
                    modal.setAttribute("style", "opacity: 0; z-index:-1;");
                    // v.changeUser(targetUserIndex);
                    result.innerHTML = " ";
                }.bind(submit, this)
            },
            showEditUserModal: function (edit) {
                let editUser = this.tableUsers.find((item) => item.firstName === edit);
                // console.log(editUser);
                // let targetUserIndex = this.tableApiUsers.findIndex((item) => item.username === edit);
                let modal = document.getElementById('updateUserModal');
                let close = document.getElementById("closeUserModal");
                let submit = document.getElementById('submitUserModal');
                let result = document.getElementById('UserModalResult');

                submit.disabled = false;

                result.innerHTML = `<div class="col-lg-12 col-sm-12 col-xs-12">
                                        <div class="row">
                                            <div class="col-lg-6 col-sm-12 col-xs-12">
                                                <div class="row">
                                                    <div class="form-group">
                                                        <label>First Name</label>
                                                        <input type="text" name="firstName" minlength="3" maxlength="30" value="${editUser.firstName}" id="editUserFirstName" required class="form-control">
                                                    </div>
                                                </div>
                                            </div>
                                            <div class="col-lg-6 col-sm-12 col-xs-12">
                                                <div class="row">
                                                    <div class="form-group">
                                                        <label>Last Name</label>
                                                        <input type="text" name="lastName" minlength="3" maxlength="30" value="${editUser.lastName}" id="editUserLastName" required class="form-control">
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="col-lg-12 col-sm-12 col-xs-12">
                                        <div class="row">
                                            <div class="form-group">
                                               <label>User email</label>
                                               <input type="email" name="userEmail" value="${editUser.email}" id="editUserEmail" required class="form-control">
                                            </div>
                                        </div>
                                    </div>
                                    <div class="col-lg-12 col-sm-12 col-xs-12">
                                        <div class="row">
                                            <div class="col-lg-6 col-sm-12 col-xs-12">
                                                 <div class="row">
                                                    <div class="form-group">
                                                        <label>User phone</label>
                                                        <input type="tel" name="userPhone" pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}" value="${editUser.phone}" id="editUserPhone" required class="form-control">
                                                    </div>
                                                 </div>
                                            </div>
                                            <div class="col-lg-6 col-sm-12 col-xs-12">
                                                 <div class="row">
                                                    <div class="form-group">
                                                        <label>Postal code</label>
                                                        <input type="number" name="userPostalCode" value="${editUser.postalCode}" id="editUserPostalCode" required class="form-control">
                                                    </div>
                                                 </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="col-lg-12 col-sm-12 col-xs-12">
                                        <div class="row">
                                            <div class="form-group">
                                                 <label>Address</label>
                                                 <input type="text" name="userAddress" value="${editUser.address1}" id="editUserAddress" required class="form-control">
                                            </div>
                                        </div>
                                    </div>
                                    <div class="col-lg-12 col-sm-12 col-xs-12">
                                        <div class="row">
                                            <div class="col-lg-6 col-sm-12 col-xs-12">
                                                <div class="row">
                                                    <div class="form-group">
                                                        <label>State</label>
                                                        <input type="text" name="userState" value="${editUser.state}" id="editUserState" required class="form-control">
                                                    </div>
                                                </div>
                                            </div>
                                            <div class="col-lg-6 col-sm-12 col-xs-12">
                                                <div class="row">
                                                    <div class="form-group">
                                                        <label>Country</label>
                                                        <input type="text" name="country" value="${editUser.country}" id="editUserCountry" required class="form-control">
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>`;

                modal.classList.remove('modal__close');
                modal.setAttribute("style", "opacity: 1; z-index:9999;");
                close.onclick = function() {
                    modal.setAttribute("style", "opacity: 0; z-index:-1;");
                    result.innerHTML = " ";
                };
                window.onclick = function(event) {
                    if (event.target == modal) {
                        modal.setAttribute("style", "opacity: 0; z-index:-1;");
                        result.innerHTML = " ";
                    }
                };
                submit.onclick = function(v, event) {
                    modal.setAttribute("style", "opacity: 0; z-index:-1;");
                    // v.changeUser(targetUserIndex);
                    result.innerHTML = " ";
                }.bind(submit, this)
            },
            addUserModal: function () {
                let modal = document.getElementById('AddUserModal');
                let close = document.getElementById("closeAddUserModal");
                let submit = document.getElementById('submitAddUserModal');
                let result = document.getElementById('AddUserModalResult');

                submit.disabled = false;

                result.innerHTML = `<div class="col-lg-12 col-sm-12 col-xs-12">
                                        <div class="row">
                                            <div class="col-lg-6 col-sm-12 col-xs-12">
                                                <div class="row">
                                                    <div class="form-group">
                                                        <label>First Name</label>
                                                        <input type="text" name="firstName" minlength="3" maxlength="30" value=" " id="editUserFirstName" required class="form-control">
                                                    </div>
                                                </div>
                                            </div>
                                            <div class="col-lg-6 col-sm-12 col-xs-12">
                                                <div class="row">
                                                    <div class="form-group">
                                                        <label>Last Name</label>
                                                        <input type="text" name="lastName" minlength="3" maxlength="30" value="" id="editUserLastName" required class="form-control">
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="col-lg-12 col-sm-12 col-xs-12">
                                        <div class="row">
                                            <div class="form-group">
                                               <label>User email</label>
                                               <input type="email" name="userEmail" value="" id="editUserEmail" required class="form-control">
                                            </div>
                                        </div>
                                    </div>
                                    <div class="col-lg-12 col-sm-12 col-xs-12">
                                        <div class="row">
                                            <div class="col-lg-6 col-sm-12 col-xs-12">
                                                 <div class="row">
                                                    <div class="form-group">
                                                        <label>User phone</label>
                                                        <input type="tel" name="userPhone" pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}" value="" id="editUserPhone" required class="form-control">
                                                    </div>
                                                 </div>
                                            </div>
                                            <div class="col-lg-6 col-sm-12 col-xs-12">
                                                 <div class="row">
                                                    <div class="form-group">
                                                        <label>Postal code</label>
                                                        <input type="number" name="userPostalCode" value="" id="editUserPostalCode" required class="form-control">
                                                    </div>
                                                 </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="col-lg-12 col-sm-12 col-xs-12">
                                        <div class="row">
                                            <div class="form-group">
                                                 <label>Address</label>
                                                 <input type="text" name="userAddress" value="" id="editUserAddress" required class="form-control">
                                            </div>
                                        </div>
                                    </div>
                                    <div class="col-lg-12 col-sm-12 col-xs-12">
                                        <div class="row">
                                            <div class="col-lg-6 col-sm-12 col-xs-12">
                                                <div class="row">
                                                    <div class="form-group">
                                                        <label>State</label>
                                                        <input type="text" name="userState" value="" id="editUserState" required class="form-control">
                                                    </div>
                                                </div>
                                            </div>
                                            <div class="col-lg-6 col-sm-12 col-xs-12">
                                                <div class="row">
                                                    <div class="form-group">
                                                        <label>Country</label>
                                                        <input type="text" name="country" value="" id="editUserCountry" required class="form-control">
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>`;

                modal.classList.remove('modal__close');
                modal.setAttribute("style", "opacity: 1; z-index:9999;");
                close.onclick = function() {
                    modal.setAttribute("style", "opacity: 0; z-index:-1;");
                    result.innerHTML = " ";
                };
                window.onclick = function(event) {
                    if (event.target == modal) {
                        modal.setAttribute("style", "opacity: 0; z-index:-1;");
                        result.innerHTML = " ";
                    }
                };
                submit.onclick = function(v, event) {
                    modal.setAttribute("style", "opacity: 0; z-index:-1;");
                    // v.changeUser(targetUserIndex);
                    result.innerHTML = " ";
                }.bind(submit, this)
            }
        }
    }
</script>

<style scoped>

</style>