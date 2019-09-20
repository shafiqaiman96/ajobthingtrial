<template>
    <section>
        <!-- NavBar -->
           <div>
            <NavBar/>
          </div>
        <br>
        <div>
            <!-- Search form -->
            <SearchBar/>
        </div>
            <br>
            <!-- Card 1 -->
            <div style="background-color: #f5f5f5; width: 100%">
              <!-- <div v-bind:key="data.id" v-for="data in jobs" class="container">
                <div class="row">
                  <div class="col"></div>
                  <div class="col-8">
                    <br>
                    <b-card>
                      <b-card-text>
                        <a :href="'job/' + data.id" class="card-link"><h3><b-img src="~/assets/img/Watsons.png" style="float: left; height: 60px; padding-right: 20px" alt="company_logo"></b-img>{{`${data.title}`}}</h3><h5>{{`${data.company}`}}</h5></a>
                      </b-card-text>
                      <div class="row">
                        <div class="col">
                          <a href="#" class="card-link"><font-awesome-icon :icon="['fas', 'briefcase']"/> {{`${data.type}`}}</a>
                          <br>
                          <a href="#" class="card-link"><font-awesome-icon :icon="['fas', 'map-marker']"/> {{`${data.location}`}}</a>
                        </div>
                        <div class="col">
                          <a href="#" class="card-link"><font-awesome-icon :icon="['fas', 'phone']"/> +{{`${data.employer_contact.phone}`}}</a>
                          <br>
                          <a href="#" class="card-link"><font-awesome-icon :icon="['fas', 'envelope']"/> {{`${data.employer_contact.email}`}}</a>
                        </div>
                      </div>
                      <br>
                      <a v-for="(value, index) in data.requirements.items">
                        {{`${value}`}} <b v-if="index < data.requirements.items.length-1">|</b>
                      </a>
                    </b-card-text>
                    <hr>
                    <div class="row">
                      <div class="col">
                        <a href="#" class="card-link"><img alt="save_job" src="~/assets/img/Path.png" style="padding-left: 100px"> Save</a>
                      </div>
                      <div class="col">
                        <b-link href="#" class="card-link"><img alt="apply_job" src="~/assets/img/Shape.png" style="padding-left: 100px"> Apply</b-link>
                      </div>
                    </div>
                  </b-card>
                </div>
                <div class="col"></div>
              </div>
                <br>
            </div> 
          </div> -->
             <!-- Card 2 -->
             <div v-bind:key="data.index" v-for="data in jobs" class="container">
                <div class="row">
                        <div class="col"></div>
                        <div class="col-8">   
                            <b-card img-src="~/assets/img/Watson-store@2x.png" img-alt="Card image" img-top>
                                <b-card-text>
                                  <h3><b-img src="~/assets/img/Watsons.png" style="float: left; height: 60px; padding-right: 20px" alt="company_logo"></b-img>{{`${data.title}`}}</h3><h5>{{`${data.company}`}}</h5>
                                </b-card-text>
                                <div class="row">
                                <div class="col">
                                  <a href="#" class="card-link"><font-awesome-icon :icon="['fas', 'briefcase']"/> {{`${data.type}`}}</a>
                                  <br>
                                  <a href="#" class="card-link"><font-awesome-icon :icon="['fas', 'map-marker']"/> {{`${data.location}`}}</a>
                                </div>
                                <div class="col">
                                  <a href="#" class="card-link"><font-awesome-icon :icon="['fas', 'phone']"/> +{{`${data.employer_contact.phone}`}}</a>
                                  <br>
                                  <a href="#" class="card-link"><font-awesome-icon :icon="['fas', 'envelope']"/> {{`${data.employer_contact.email}`}}</a>
                               </div>
                            </div></b-card-text>
                                <hr>
                                <div class="row">
                                    <div class="col">
                                        <a href="#" class="card-link"><img alt="save_job" src="~/assets/img/Path.png" style="padding-left: 100px"> Save</a>
                                    </div>
                                    <div class="col">
                                        <b-link href="#" class="card-link"><img alt="apply_job" src="~/assets/img/Shape.png" style="padding-left: 100px"> Apply</b-link>
                                    </div>
                                </div>
                            </b-card>
                        </div>
                        <div class="col"></div>
                </div>
            </div> -->

         <br>

        <div v-bind:key="data.index" v-for="data in jobs" class="container">
            <div class="row">
                <div class="col"></div>
                    <div class="col-8">
                        <b-card title="Requirements">
                            <b-card-text>
                              <hr>
                            </b-card-text>
                            <b-card-text> 
                                <ul>
                                  <li v-bind:key="item.index" v-for="item in data.requirements.items">{{`${item}`}}</li>
                                </ul>
                            </b-card-text>
                        </b-card>
                    </div>
                    <div class="col"></div>
                </div>
            </div>
        <br>

        <div v-bind:key="data.index" v-for="data in jobs" class="container">
            <div class="row">
                <div class="col"></div>
                    <div class="col-8">
                        <b-card title="Responsibilities">
                            <b-card-text>
                              <hr>
                            </b-card-text>
                            <b-card-text> 
                                <ul>
                                  <li v-bind:key="respon.index" v-for="respon in data.responsibilites">{{`${respon}`}}</li>
                                </ul>
                            </b-card-text>
                        </b-card>
                    </div>
                    <div class="col"></div>
                </div>
            </div>
        <br> 

         <div v-bind:key="data.index" v-for="data in jobs" class="container">
            <div class="row">
                <div class="col"></div>
                    <div class="col-8">
                        <b-card title="Additional Benefits">
                            <b-card-text>
                              <hr>
                            </b-card-text>
                            <b-card-text> 
                                <ul>
                                  <li v-bind:key="benefit.index" v-for="benefit in data.benefit">{{`${benefit}`}}</li>
                                </ul>
                            </b-card-text>
                        </b-card>
                    </div>
                    <div class="col"></div>
                </div>
            </div> 
        </div> 
    </section>
</template>

<script>
import axios from 'axios'
import SearchBar from './searchbar.vue'
import NavBar from './navbar.vue'

export default {
  name: 'searchbar',

  components: {
    SearchBar,
    NavBar
  },

  data () {
    return {
      jobs: []
    }
  },

  mounted () {
    axios
      .get('http://private-27298f-frontendtestmaukerja.apiary-mock.com/jobs')
      .then(response => {
        this.jobs = response.data
      })
      .catch(err => {
        console.log(err)
      })
  }
}
</script>