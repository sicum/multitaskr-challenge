<template>
  <div>
    <div class="container">
      <h1>Leads in</h1>
      <SearchLeads/>
      <div>
        <b-link v-b-toggle.collapse-1 class="button-collapse">
          <span class="when-opened">
               <fa icon="chevron-up" />
           </span>
           <span class="when-closed">
               <fa icon="chevron-down" />
           </span>
          Today
        </b-link>
        <b-collapse id="collapse-1" visible class="mt-2">
          <TableLeads :data="data.today"/>
        </b-collapse>
      </div>
      <div>
        <b-link v-b-toggle.collapse-2 class="button-collapse">
          <span class="when-opened">
               <fa icon="chevron-up" />
           </span>
           <span class="when-closed">
               <fa icon="chevron-down" />
           </span>
          Yesterday
        </b-link>
        <b-collapse visible id="collapse-2" class="mt-2">
          <TableLeads :data="data.yesterday"/>
        </b-collapse>
      </div>
      <div>
        <b-link v-b-toggle.collapse-3 class="button-collapse">
          <span class="when-opened">
               <fa icon="chevron-up" />
           </span>
           <span class="when-closed">
               <fa icon="chevron-down" />
           </span>
          Everithing else
        </b-link>
        <b-collapse id="collapse-3" class="mt-2">
          <TableLeads :data="data.everything"/>
        </b-collapse>
      </div>
    </div>
  </div>
</template>
<style scoped>
  .collapsed > .when-opened,:not(.collapsed) > .when-closed {
      display: none;
  }
  .button-collapse {
    text-decoration: none;
    color: black;
    font-weight: bold;
  }
</style>
<script>
  export default {
    data(){
      return {
        data: {
          "today": [
            {
              "datetime": "5:30 PM",
              "name": "Stephen King",
              "id": "0008 0019",
              "image":"https://source.unsplash.com/random/100x100",
              "email": "stephen.king@hey.com",
              "phone": "619 520 6310",
              "verticals": [
                "ADU", "Solar"
              ],
              "updated": "4 hours ago"
            },
            {
              "datetime": "Taken",
              "name": "William Shakespeare",
              "id": "0003 0007 0018",
              "image":"https://source.unsplash.com/random/100x100",
              "email": "william.shakespeare@hey.com",
              "phone": "619 631 7421",
              "verticals": [
                "Landscape", "ADU", "Solar"
              ],
              "updated": "One hours ago"
            }
          ],
          "yesterday" : [
            {
              "datetime": "Taken",
              "name": "Leo Tolstay",
              "id": "0017",
              "image":"https://source.unsplash.com/random/100x100",
              "email": "leo.tolstay@hey.com",
              "phone": "619 742 8532",
              "verticals": [
                "ADU"
              ],
              "updated": "Jun 23"
            },
            {
              "datetime": "Taken",
              "name": "Charls Dickens",
              "id": "0018",
              "image":"https://source.unsplash.com/random/100x100",
              "email": "charls.dickens@hey.com",
              "phone": "619 742 8532",
              "verticals": [
                "ADU"
              ],
              "updated": "Jun 23"
            },
            {
              "datetime": "Taken",
              "name": "James Joyce",
              "id": "0015",
              "image":"https://source.unsplash.com/random/100x100",
              "email": "james.joyce@hey.com",
              "phone": "619 964 0754",
              "verticals": [
                "ADU"
              ],
              "updated": "Jun 23"
            }
          ],
          "everything":[
            {
              "datetime": "Taken",
              "name": "Ernest Hemingway",
              "id": "0014",
              "image":"https://source.unsplash.com/random/100x100",
              "email": "ernest.hemingway@hey.com",
              "phone": "619 075 1865",
              "verticals": [
                "ADU"
              ],
              "updated": "Jun 22"
            },
            {
              "datetime": "Taken",
              "name": "Jane Austen",
              "id": "0013",
              "image":"https://source.unsplash.com/random/100x100",
              "email": "jane.austen@hey.com",
              "phone": "619 186 2976",
              "verticals": [
                "ADU"
              ],
              "updated": "Jun 22"
            },
            {
              "datetime": "Taken",
              "name": "F. Scott Fitzgerald",
              "id": "0012",
              "image":"https://source.unsplash.com/random/100x100",
              "email": "f.scott.fitzgerald@hey.com",
              "phone": "619 297 3087",
              "verticals": [
                "ADU"
              ],
              "updated": "Jun 22"
            },
            {
              "datetime": "Taken",
              "name": "Mark Twain",
              "id": "0011",
              "image":"https://source.unsplash.com/random/100x100",
              "email": "mark.twain@hey.com",
              "phone": "619 308 4198",
              "verticals": [
                "ADU"
              ],
              "updated": "Jun 19"
            },
            {
              "datetime": "Taken",
              "name": "Marcel Proust",
              "id": "0010",
              "image":"https://source.unsplash.com/random/100x100",
              "email": "marcel.proust@hey.com",
              "phone": "619 419 5209",
              "verticals": [
                "ADU"
              ],
              "updated": "Jun 19"
            }
          ]
        }
      }
    }
  }
</script>
