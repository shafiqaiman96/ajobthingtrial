<template>
  <div class="container" style="background-color: white;">
  <div class="col-12">
     <div class="row" style="background-color: white; width: 100%">
        <div class="col-10">
          <div class="row">
            <div class="col-sm-4"><input class="form-control" type="text" placeholder="Job title, company" aria-label="Search"></div>
            <div class="col-sm-4"><input class="form-control" type="text" placeholder="Location" aria-label="Search"></div>
            <div class="col-sm-4">
              <b-form-select v-model="selected" class="form-control" size="sm">
                <option :value="null" size="sm">Min Salary (MYR)</option>
                <option value="a">RM 1,500</option>
                <option value="b">RM 3,000</option>
                <option value="c">RM 5,000</option>
                <option value="c">RM 10,000 & above</option>
                <div class="mt-2">Selected: <strong>{{ selected }}</strong></div>
              </b-form-select>
            </div>
          </div>
        </div>
        <div class="col-sm-2"><button class="form-control" style="background-color: #db1435; color: #fff; padding-top: 2.5px"><font-awesome-icon :icon="['fas', 'search']"/> Search</button> </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  data () {
    return {
      selected: null
    }
  }
}
</script> 

<style scoped>

.navbar.navbar-dark.bg-dark{
    background-color: #db1435!important;
 }

.nav-link{
    color: #fff;
    background-color: #be2a43;
     }

.nav-link:not(.active){
    color: #fff;
    background-color: #db1435;
}



.form-control {
max-width:300px;
max-height: 30px;
border-bottom-left-radius:20px;
border-bottom-right-radius:20px;
border-top-left-radius:20px;
border-top-right-radius:20px}

</style>