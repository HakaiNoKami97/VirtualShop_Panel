<template>
    <div>
          <Sidebar />
          <div class="main-content">
  
              <TopNav />
  
              <div class="container-fluid">
                  <div class="row justify-content-center">
                      <div class="col-12 col-lg-10 col-xl-8">
  
                          <!-- Header -->
                          <div class="header mt-md-5">
                              <div class="header-body">
                                  <div class="row align-items-center">
                                  <div class="col">
  
                                      <!-- Pretitle -->
                                      <h6 class="header-pretitle">
                                      Ingreso 
                                      </h6>
  
                                      <!-- Title -->
                                      <h1 class="header-title">
                                          <b>Ingresos</b>
                                      </h1>
  
                                  </div>
                                  </div> <!-- / .row -->
                                  <div class="row align-items-center">
                                  <div class="col">
  
                                      <!-- Nav -->
                                      <ul class="nav nav-tabs nav-overflow header-tabs">
                                      <li class="nav-item">
                                          <a class="nav-link active">
                                          Ingresos
                                          </a>
                                      </li>
                                      <li class="nav-item">
                                          <router-link class="nav-link" to="/ingreso/create">Nuevo ingreso</router-link>
                           
                                          
                                      </li>
                                      
                                      </ul>
  
                                  </div>
                                  </div>
                              </div>
                          </div>
  
                          <div class="row mb-5">
                              <div class="col-9 d-flex">
                                  <input type="date" class="form-control" style="margin-right: 1rem"/>
                                  <input type="date" class="form-control"/>
                              </div>
                              <div class="col">
                                  <button class="btn btn-primary" style="width:100%">Buscar</button>
                              </div>
                          </div>
  
                          <div class="card">
                              <div class="card-header">
  
                                  <!-- Title -->
                                  <h4 class="card-header-title mb-0">
                                      <b>Ingreso a inventario</b>
                                  </h4>
  
                              </div>
                              <div class="table-responsive">
                                  <table class="table table-sm table-nowrap card-table">
                                  <thead>
                                      <tr>
                                      <th>Invoice ID</th>
                                      <th>Date</th>
                                      <th>Amount</th>
                                      <th>Status</th>
                                      </tr>
                                  </thead>
                                  <tbody class="fs-base">
                                      <tr>
                                      <td>
                                          <a href="invoice.html">Invoice #10395</a>
                                      </td>
                                      <td>
                                          <time datetime="2020-04-24">Apr. 24, 2020</time>
                                      </td>
                                      <td>
                                          $29.00
                                      </td>
                                      <td>
                                          <span class="badge bg-secondary">Outstanding</span>
                                      </td>
                                      </tr>
                                      <tr>
                                      <td>
                                          <a href="invoice.html">Invoice #10244</a>
                                      </td>
                                      <td>
                                          <time datetime="2020-03-24">Mar. 24, 2020</time>
                                      </td>
                                      <td>
                                          $29.00
                                      </td>
                                      <td>
                                          <span class="badge bg-success">Paid</span>
                                      </td>
                                      </tr>
                                      <tr>
                                      <td>
                                          <a href="invoice.html">Invoice #10119</a>
                                      </td>
                                      <td>
                                          <time datetime="2020-02-24">Feb. 24, 2020</time>
                                      </td>
                                      <td>
                                          $29.00
                                      </td>
                                      <td>
                                          <span class="badge bg-success">Paid</span>
                                      </td>
                                      </tr>
                                      <tr>
                                      <td>
                                          <a href="invoice.html">Invoice #10062</a>
                                      </td>
                                      <td>
                                          <time datetime="2020-01-24">Jan. 24, 2020</time>
                                      </td>
                                      <td>
                                          $29.00
                                      </td>
                                      <td>
                                          <span class="badge bg-success">Paid</span>
                                      </td>
                                      </tr>
                                  </tbody>
                                  </table>
                              </div>
                          </div>
                          
                          
  
                      </div>
                  </div> <!-- / .row -->
              </div>
              
  
          </div>
          
      </div>
  </template>
  
  <script>
  // @ is an alias to /src
  
  import Sidebar from '@/components/Sidebar.vue';
  import TopNav from '@/components/TopNav.vue';
  
  export default {
    name: 'IndexIngresoApp',
    components: {
      Sidebar,
      TopNav
    }
  }
  </script>
  