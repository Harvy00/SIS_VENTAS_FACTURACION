<template>
<layout fluid>
    <v-flex >
    <v-app id="inspire">
    <v-navigation-drawer
      :clipped="$vuetify.breakpoint.lgAndUp"
      v-model="drawer"
      fixed
      app
    >
      <v-list dense class="marge">
        <template>
          <!-- <v-list-item :to="{name: 'home'}"> -->
          <v-list-item :to="{name: ''}">

            <v-list-item-action >
              <v-icon color= "#c59803">home</v-icon>
            </v-list-item-action >
            <v-list-item-title color="Pink"> </v-list-item-title>
            <v-list-item-title >Inicio
            </v-list-item-title >
          </v-list-item  >
        </template>
        <!-- ----------------------------------------- -->

        <template>
            <v-list-group color= "rgb(243, 234, 234)" >
            <v-list-item slot="activator">
              <v-list-item-content >
                <v-list-item-title >
                  Almacén
                  
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item >
            <v-list-item  :to="{ name: 'categoria' }">
              
              <v-list-item-action>
                <v-icon color= "#c59803">fact_check</v-icon>
              </v-list-item-action>
              <v-list-content >
                <v-list-title>
                  Categorías
                </v-list-title>
              </v-list-content>
            </v-list-item>
            <v-list-item :to="{ name: ''}">
              <v-list-action>
                <v-icon color= "#c59803" >article</v-icon>
              </v-list-action>
              <v-list-item-content>
                <v-list-title>
                  Aticulos
                </v-list-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-group>
        </template>
        <template>
            <v-list-group color= "rgb(243, 234, 234)">
            <v-list-item slot="activator">
              <v-list-item-content  >
                <v-list-item-title>
                  Compras
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item :to="{ name: ''}">
              <v-list-action>
                <v-icon color= "#c59803">paid</v-icon>
              </v-list-action>
              <v-list-tile-content>
                <v-list-title>
                  Ingresos
                </v-list-title>
              </v-list-tile-content>
            </v-list-item>
            <v-list-item :to="{ name: ''}">
              <v-list-tile-action>
                <v-icon color= "#c59803" > local_shipping</v-icon>
              </v-list-tile-action>
              <v-list-tile-content>
                <v-list-title>
                  Proveedores
                </v-list-title>
              </v-list-tile-content>
            </v-list-item>
          </v-list-group>
        </template>
        <template>
            <v-list-group color= "rgb(243, 234, 234)">
            <v-list-item slot="activator">
              <v-list-item-content>
                <v-list-item-title>
                  Ventas
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item :to="{ name: ''}">
              <v-list-tile-action>
                <v-icon color= "#c59803">point_of_sale</v-icon>
              </v-list-tile-action>
              <v-list-tile-content>
                <v-list-tile-title>
                  Ventas
                </v-list-tile-title>
              </v-list-tile-content>
            </v-list-item>
            <v-list-item :to="{ name: ''}">
              <v-list-tile-action>
                <v-icon color= "#c59803">groups</v-icon>
              </v-list-tile-action>
              <v-list-tile-content>
                <v-list-tile-title>
                  Clientes
                </v-list-tile-title>
              </v-list-tile-content>
            </v-list-item>
          </v-list-group>
        </template>
        <template>
            <v-list-group color= "rgb(243, 234, 234)">
            <v-list-item slot="activator">
              <v-list-item-content>
                <v-list-item-title>
                  Accesos
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item :to="{ name: ''}">
              <v-list-tile-action>
                <v-icon color= "#c59803">switch_account</v-icon>
              </v-list-tile-action>
              <v-list-tile-content>
                <v-list-tile-title>
                  Roles
                </v-list-tile-title>
              </v-list-tile-content>
            </v-list-item>
            <v-list-item :to="{ name: ''}">
              <v-list-tile-action>
                <v-icon color= "#c59803">perm_identity</v-icon>
              </v-list-tile-action>
              <v-list-tile-content>
                <v-list-tile-title>
                  Usuarios
                </v-list-tile-title>
              </v-list-tile-content>
            </v-list-item>
          </v-list-group>
        </template>
        <template>
            <v-list-group color= "rgb(243, 234, 234)">
                <v-list-item slot="activator">
                  <v-list-item-content>
                    <v-list-item-title>
                      Consultas
                    </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item :to="{ name: ''}">
                  <v-list-action>
                    <v-icon color= "#c59803">manage_search</v-icon>
                  </v-list-action>
                  <v-list-item-content>
                    <v-list-title>
                      Consulta Compras
                    </v-list-title>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item :to="{ name: ''}">
                  <v-list-action>
                    <v-icon color= "#c59803">manage_search</v-icon>
                  </v-list-action>
                  <v-list-item-content>
                    <v-list-title>
                      Consulta Ventas
                    </v-list-title>
                  </v-list-item-content>
                </v-list-item>
          </v-list-group>
        </template>
         <!-- ----------------------------------------- -->
      </v-list>

  </v-navigation-drawer>

 <!--    <div class="Glen"> -->
        <v-toolbar class="nvar"
          :clipped-left="$vuetify.breakpoint.lgAndUp"
          color="orange -3"
          dark
          app
          fixed
        >
            <v-toolbar-title style="width: 300px" class="ml-0 pl-3">
              
            <v-btn  @click.stop="drawer = !drawer" icon>
            <v-icon>menu</v-icon>
            </v-btn>
            <span class="hidden-sm-and-down">Sistema
            </span>
          </v-toolbar-title>
         <v-spacer></v-spacer>
             <v-btn icon>
            <v-icon>apps</v-icon>
            </v-btn>
          
    </v-toolbar>
<!--    </div> -->
    
    <v-content>
      <v-container>
        <v-slide-y-transition mode="out-in">
          <router-view/>
        </v-slide-y-transition>
      </v-container>
    </v-content>
<!-- ------------------------------------------------------------------- -->

<div class="Footer">
  <div class="Footer2">
    Sistema &copy;2021
  </div> 
    <!-- <v-footer dark class="Footer2" >
          <v-layout justify-center>
            <v-flex text-xs-center>
              <v-card flat tile color="primary" class="white--text">
                <v-card-text class="white--text pt-0">
                  Sistema &copy;2021
                </v-card-text>
              </v-card>
            </v-flex>
          </v-layout>
        </v-footer>  -->
</div>
  </v-app>
  </v-flex>
  </layout>
     

</template>


<style>
.marge{
  margin-top: 70px;
  z-index: 1;
}
.nvar{
  z-index: 5;
  max-height: 70px;
  position: fixed;
}

.Footer{
 z-index: 5;
 height: 50px;
 background: #007BFF;
 width: 100%;
 }

.Footer2{
 height: 100%;
 width: 100%;
 text-align: center;
 color: rgb(220, 220, 220);
 background-color: #c59803;
 margin-top: 20px;
}

.Glen{
  z-index: 5;
  width: 100%;
  max-height: 70px;
  position: fixed;
}
.v-list-item__action{
color: darkblue;

            }
          
.v-navigation-drawer__content {
  background-color: rgb(43, 43, 126);
}

</style>

<script>

export default {
  name: 'App',

  data: () => ({
    drawer: null,
  }),
};
</script>

