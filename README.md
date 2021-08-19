# tabulator-demo

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```


### Tabulator Documentation
See [Configuration Reference](http://tabulator.info/docs/4.9).


### Sauce
```
<template>
  <div id="app">
    <div id="example-table"></div>
  </div>
</template>

<script>
import Tabulator from 'tabulator-tables';
export default {
  name: "App",
  data() {
    return {
      table: null,
      tableData: [
      {
        id: 1,
        name: "Billy Bob",
        age: "12",
        gender: "male",
        height: 1,
        col: "red",
        dob: "",
        cheese: 1,
      },
      {
        id: 2,
        name: "Mary May",
        age: "1",
        gender: "female",
        height: 2,
        col: "blue",
        dob: "14/05/1982",
        cheese: true,
      },
    ]};
  },
  mounted() {

    this.table = new Tabulator("#example-table", {
      data: this.tableData, //set initial table data
      columns: [
        { title: "Name", field: "name" },
        { title: "Age", field: "age" },
        { title: "Gender", field: "gender" },
        { title: "Height", field: "height" },
        { title: "Favourite Color", field: "col" },
        { title: "Date Of Birth", field: "dob" },
        { title: "Cheese Preference", field: "cheese" },
      ],
    });
  },
};
</script>

<style lang="scss">
@import  "~vue-tabulator/dist/scss/bootstrap/tabulator_bootstrap4";
#app {

}
</style>

```
