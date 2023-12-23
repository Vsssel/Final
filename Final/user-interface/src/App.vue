<script>
import Sidebar from './components/Sidebar.vue'
import SidebarLogo from './components/SidebarLogo.vue'
import logo from './assets/logo.svg'


export default{
  components:{
    Sidebar,
    SidebarLogo,
  },
  data(){
    return{
      wrapperStyle:{
        width: '55%',
        height: '70px',
        position: 'relative',
        display: 'flex',
        alignItems: 'center',
        justifyContent: 'space-between',
        padding: '10px'
      },
      imgStyle:{
        width: '27px',
      },
      textStyle:{
        fontSize: '18px',
        fontWeight: '600',
      },
      logo: logo,
      items: [
        {
          dropdown: true,
          dropdownContent: [{label: 'Sales Analytics', route:''}, {label: 'Seller Profiles', route: ''}, {label:'Revenue by Period'}],
          buttonText: 'Dashboard'
        },
        {
          dropdown: true,
          dropdownContent: [{label: 'Top Products', route:''}, {label: 'Product Grid', route: ''}, {label:'Product Management', route:''}, {label:'Product Categories', route: ''}, {label: 'Add New Product', route: ''}],
          buttonText: 'Products'
        },
        {
          label: 'Orders',
          route: '',
        },
        {
          label: 'Statistics',
          route: '',
        },
        {
          label: 'Reviews',
          route: ''
        },
        {
          label: 'Customers',
          route: '',
        },
        {
          label: 'Transactions',
          route: '',
        },
        {
          label: 'Settings',
          route: ''
        }
      ],
      sidebarWrapperStyle:{
        width: '100%',
        position: 'relative',
      },
      buttonStyle:{
        width: '90%',
        backgroundColor: 'white',
        color: 'black',
        fontSize: '14px',
        fontWeight: '500',
        border: 'none',
        padding: '10px',
        textAlign: 'start',
      },
      contentStyle:{
        width: '90%',
        backgroundColor: 'white',
        color: 'black',
        fontSize: '12px',
        fontWeight: '500',
        border: 'none',
        padding: '10px',
        textAlign: 'start',
      }
    }
  },
}
</script>

<template>
  <div class="side-wrapper">
    <SidebarLogo :src="logo" :wrapperStyle="wrapperStyle" :imgStyle="imgStyle" :textStyle="textStyle">ShopPoint</SidebarLogo>
    <Sidebar :items="items" :buttonStyle="buttonStyle" :contentStyle="contentStyle"></Sidebar>
  </div>
</template>

<style>
*{
  font-family: Verdana, Geneva, Tahoma, sans-serif;
}
.side-wrapper{
  width: 270px;
  height: 100vh;
  background-color: aqua;
  text-decoration: ;
}
</style>
