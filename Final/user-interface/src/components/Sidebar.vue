
<template>
    <div class="sidebarContent" v-for="item in items">
        <DropdownButton :buttonText="item.buttonText" v-if="item.dropdown" :buttonStyle="buttonStyle">
            <Button v-for="content in item.dropdownContent" :styleValues="contentStyle">
                <router-link :to="content.route"><li>{{ content.label }}</li></router-link>
            </Button>
        </DropdownButton>
        <Button v-else :styleValues="buttonStyle">
          <router-link :to="item.route">{{ item.label }}</router-link>
        </Button>
    </div>
  </template>
  
<script>
import Button from './Button.vue'
import DropdownButton from './DropdownButton.vue'
  export default {
    components:{
        Button,
        DropdownButton
    },
    props:{
        items: Array,
        buttonText: String,
        buttonStyle: Object,
        contentStyle: Object,
    }
  };
  </script>
  