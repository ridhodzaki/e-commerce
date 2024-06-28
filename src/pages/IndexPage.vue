<template>
  <q-page class="q-pa-md">
    <div class="items-center flex flex-center column q-px-xls" :style="`height:${this.$q.screen.xs || this.$q.screen.sm ? '50vh' : '100vh'} `">
      <span :class="`text-primary text-center text-weight-bold ${this.$q.screen.xs || this.$q.screen.sm ? 'text-h6' : 'text-h4 '}`">PasarKita</span>
      <span :class="`text-weight-bold text-center ${this.$q.screen.xs || this.$q.screen.sm ? 'text-h5' : 'text-h1 q-mt-lg'}`">Discover Everything You Need Right Here!</span>
      <span :class="`text-center ${this.$q.screen.xs || this.$q.screen.sm ? 'text-body' : 'text-body1 q-px-xl  q-mt-xl'}`">"With PasarKita, you can explore various product categories, enjoy daily discounts, and get your selected items with fast delivery and responsive customer service."</span>
    </div>
    <div class="q-pa-xl">
      <div class="q-pa-md" id="popular_product">
        <div class="text-h5 text-weight-medium text-center">Categories</div>
        <div class="q-mt-md justify-center row">
          <div
            v-for="(categori, i) in listkategoris"
            :key="i"
            class="col-md-2 col-sm-6 col-xs-12 q-pa-md">
            <q-btn no-caps  style="width: 100%">
              <div class="column flex flex-center q-pa-sm">
                <q-icon :name="categori.icon" size="md"/>
                <span>{{ categori.name }}</span>
              </div>
            </q-btn>
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  data () {
    return {
      listkategoris: [
        {
          name: 'Watch',
          icon: 'watch'
        },
        {
          name: 'Phone',
          icon: 'phone_iphone'
        },
        {
          name: 'Headphone',
          icon: 'headphones'
        },
        {
          name: 'Computer',
          icon: 'computer'
        },
        {
          name: 'Controller',
          icon: 'videogame_asset'
        },
        {
          name: 'Speaker',
          icon: 'speaker'
        }
      ]
    }
  }
}
</script>
