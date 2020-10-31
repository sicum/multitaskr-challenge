<template>
<div>
  <div v-if="items.length > 0">
    <table class="table">
      <div class="card-row-head">
        <div class="row">
          <div class="item col-1"></div>
          <div class="item col-3">Name</div>
          <div class="item col-2">Email</div>
          <div class="item col-1">Phone</div>
          <div class="item col-2">Verticals</div>
          <div class="item col-2">Updated</div>
          <div class="item col-1"></div>
        </div>
      </div>
      <div class="card mt-2 mb-2" v-for="(item) in items">
        <div class="card-body p-2">
          <div class="row">
            <div class="item col-1 p-3 separator">
              <p class="m-0 text-muted"><span><fa :class="(item.datetime != 'Taken')?'active-deal':''" icon="calendar-day"/></span> {{item.datetime}}</p>
            </div>
            <div class="item col-3 pt-1"> 
              <div class="row">
                <div class="col-3 pl-2 pr-0">
                  <img :src="item.image" class="rounded-circle" height="40px" width="40px">
                </div>
                <div class="col-9 pl-0">
                  <p class="m-0 purple-text">{{item.name}}</p>
                  <p class="m-0"><span class="text-muted">Deal ID: </span>{{item.id}}</p>
                </div>
              </div>
            </div>
            <div class="item col-2 pt-3">{{item.email}}</div>
            <div class="item col-1 pt-3">{{item.phone}}</div>
            <div class="item col-2 pt-3">
              <div v-if="item.verticals.length > 0">
                <span class="badge badge-secondary" v-for="vertical in item.verticals">{{vertical}}</span>
              </div>
            </div>
            <div class="item col-2 pt-3 pl-4">
              {{item.updated}}
            </div>
            <div class="item col-1 pt-1">
              <b-dropdown text="..." variant="link">
                <b-dropdown-item href="#">Option a</b-dropdown-item>
                <b-dropdown-item href="#">Option b</b-dropdown-item>
                <b-dropdown-item href="#">Option c</b-dropdown-item>
              </b-dropdown>
            </div>
          </div>
        </div>
      </div>
    </table>
  </div>
  <div v-else>
    <div class="card mb-2">
      <div class="card-body">
        <p class="m-0 text-muted text-center">Can't find data</p>
      </div>
    </div>  
  </div>
</div>
</template>
<script>
  export default {
    props: ['data'],
    data(){
      return {
        items : [],
      }
    },
    mounted() {
      if (this.data) {
        this.items = this.data;
      }
    }
  }
</script>
<style>
  .active-deal {
    color:#58FA82;
  }
  .dropdown-toggle {
    color: #4813B0;
    font-weight: bold;
    cursor:pointer;
  }
  .dropdown-toggle::after{
    display: none;
  }
  .purple-text {
    color: #4813B0;
    font-weight: bold;
  }
  .card-row-head {
    color: #ced4da;
    font-weight: bold;
    position: relative;
    display: table-row;
    flex-direction: row;
    min-width: 0;
    word-wrap: break-word;
    background-color: #fff;
  }
  .card-row {
    position: relative;
    display: table-row;
    flex-direction: row;
    min-width: 0;
    word-wrap: break-word;
    background-color: #fff;
    background-clip: border-box;
    border: 1px solid rgba(0, 0, 0, 0.125);
    border-radius: 0.25rem;
  }
  .item {
    font-size: 12px;
    white-space: nowrap;
  }
  .separator {
    border-right: 1px solid rgba(0, 0, 0, 0.125);
  }
</style>