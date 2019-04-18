<template lang="html">
  <div class="container-scroller">
    <app-header></app-header>
    <div class="container-fluid page-body-wrapper">
      <app-sidebar></app-sidebar>
      <div class="main-panel">
        <div class="content-wrapper">
          <section class="dashboard">
             <div class="row">
                <div class="col-lg-12 grid-margin">
                    <div class="card">
                        <div class="card-body d-flex justify-content-center">
                        <button class="btn btn-primary">Buy new domain</button>
                        </div>
                    </div>
                </div>
             </div>
             <div class="row">
                <div class="col-lg-12 grid-margin">
                    <div class="card">
                        <div class="card-body">
                            <data-tables
                             :data="tableData"
                             :loading="loading">
                            <el-table-column
                            prop = "domainName"
                            label = "Domain name"
                            >
                            </el-table-column>
                            <el-table-column
                            prop = "expiration"
                            label = "Expiration"
                            >

                            </el-table-column>
                            <el-table-column
                            prop = "actions"
                            label = "Actions"
                            >
                            <template slot-scope="props">
                                <button class="btn btn-danger" v-if="props.row.domainName === 'expired.domain.tld'">Reactivate</button>
                                <button class="btn btn-warning" v-else>Renew</button>
                            </template>
                            </el-table-column>
                            </data-tables>
                        </div>
                    </div>
                </div>
             </div>
          </section>
        </div>
        <app-footer></app-footer>
      </div>
    </div>
  </div>
</template>

<script lang="js">
// @ is an alias to /src
import AppHeader from '@/components/AppHeader'
import AppSidebar from '@/components/AppSidebar'
import AppFooter from '@/components/AppFooter'
import AppConfTabs from '@/components/AppConfTabs'

export default {
  name: 'home',
  components: {
    AppHeader,
    AppSidebar,
    AppFooter,
    AppConfTabs
  },
  data(){
      return{
          tableData: [],
          loading: false
      }
  },
  computed: {
    expirationDate: function () {
        var today = new Date();
        var dd = String(today.getDate());
        var mm = String(today.getMonth() - 2);
        var yyyy = today.getFullYear();

        today = dd + '.' + mm + '.' + yyyy;

        return today;
    }
  },
  mounted(){
      this.loadTableData();
  },
  methods: {
      loadTableData: function () {
          let dt =[
              {
                  "domainName" : "expired.domain.tld",
                  "expiration" : "n"
              },
              {
                  "domainName" : "expires.soon.tld",
                  "expiration" : "n"
              },
              {
                  "domainName" : "cool.domain.tld",
                  "expiration" : "n"
              },
              {
                  "domainName" : "nice.domain.tld",
                  "expiration" : "n"
              }
          ]
        dt.forEach((item, index) => {
           console.log(item);
           if (item.domainName === "expired.domain.tld") {
              var expired = new Date();
              var dd = String(expired.getDate() + 3);
              var mm = String(expired.getMonth() - 2);
              var yyyy = expired.getFullYear();

              expired = dd + '.' + mm + '.' + yyyy;
               item.expiration = expired;

//                index.classList.add('red');

           } else if (item.domainName === "expires.soon.tld") {
              var expires = new Date();
              var dd = String(expires.getDate());
              var mm = String(expires.getMonth()+ 2);
              var yyyy = expires.getFullYear();

              expires = dd + '.' + mm + '.' + yyyy;
              item.expiration = expires;
          } else{
              var cool = new Date();
              var dd = String(cool.getDate());
              var mm = String(cool.getMonth()+ 5);
              var yyyy = cool.getFullYear();

              cool = dd + '.' + mm + '.' + yyyy;
              item.expiration = cool;
          }
        });
          this.tableData = dt;
      }
  }
}
</script>

<style lang="scss">
    .red {
        color: red;
    }
</style>
