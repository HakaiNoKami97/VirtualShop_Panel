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
                                    Ventas 
                                    </h6>

                                    <!-- Title -->
                                    <h1 class="header-title">
                                        <b>Ventas</b>
                                    </h1>

                                </div>
                                </div> <!-- / .row -->
                                
                            </div>
                        </div>

                        <div class="row mb-5">
                            <div class="col-9 d-flex">
                                <input type="date" class="form-control" v-model="inicio" style="margin-right: 1rem"/>
                                <input type="date" class="form-control" v-model="hasta"/>
                            </div>
                            <div class="col">
                                <button class="btn btn-primary" style="width:100%" v-on:click="init_data()">Buscar</button>
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
                                        <th>Proveedor</th>
                                        <th>Serie</th>
                                        <th>Monto</th>
                                        <th>Documento</th>
                                        <th>*</th>
                                    </tr>
                                </thead>
                                <tbody class="fs-base" v-if="ventas.length >= 1">
                                    <tr v-for="item in ventas">
                                        <td>
                                            <a>{{item.proveedor}}</a>
                                        </td>
                                        <td>
                                            <a>#{{item.serie.toString().padStart(6,'000000')}}</a>
                                        </td>
                                        <td>
                                            {{convertCurrency(item.monto_resultante)}}
                                        </td>
                                        <td>
                                            <a :href="$url+'/obtener_comprobante_ingreso/'+item.documento" target="_blank">
                                                <span class="badge bg-success">Abrir documento</span>
                                            </a>
                                        </td>
                                        <td>
                                            <button class="btn btn-primary btn-sm">
                                                <router-link style="    color: #ffffff !important;" :to="{name: 'ingreso-detalle',params: {id: item._id}}">Ver detalles</router-link>
                                            </button>
                                          
                                        </td>
                                    </tr>
                                    
                                </tbody>
                                <tbody v-if="ventas.length == 0">
                                    <tr>
                                        <td colspan="4">
                                            <div class="row justify-content-center">
                                                    <div class="col-12 col-md-6 col-xl-6 my-5">
                                                        
                                                        <div class="text-center">
                                                        
                                                        <!-- Preheading -->
                                                        <h6 class="text-uppercase text-muted mb-4">
                                                            404 error
                                                        </h6>

                                                        <!-- Heading -->
                                                        <h1 class="display-4 mb-3">
                                                            No se encontraron registros 😭
                                                        </h1>

                                                        <!-- Subheading -->
                                                        <p class="text-muted mb-4">
                                                            No hay datos que mostrar!
                                                        </p>

                                                
                                                        
                                                        </div>

                                                    </div>
                                                </div>  
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

import Sidebar from '@/components/Sidebar.vue'
import Topnav from '@/components/TopNav.vue'

export default {
    name: 'VentaIndexApp',
    data() {
        return {
            inicio: '',
            hasta: '',
            ventas: []
        }
    },
    methods:{
        init_data(){

        }
    },  
    components: {
        Sidebar,
        Topnav
    }
}
</script>