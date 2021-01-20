<template>
  <div class="col-12 q-ml-xs q-mr-md q-col-gutter-md row">
  <q-item
    clickable
    tag="a"
    target="_blank"
    :href="link"
  >
    <q-item-section
      v-if="icon"
      avatar
    >
      <q-icon :name="icon" />
    </q-item-section>

    <q-item-section>
      <q-item-label>{{ title }}</q-item-label>
      <q-item-label caption>
        {{ caption }}
      </q-item-label>
    </q-item-section>
  </q-item>
        <div class="col-md-3 col-sm-12 col-xs-12">
            <!-- card1 -->
            <q-card bordered>
                <q-card-section>
                    <div class="row items-center no-wrap">
                        <div class="col q-pl-sm">
                            <div class="text-h6">Our Planet</div>
                            <div class="text-subtitle2">by John Doe</div>
                        </div>
                        <div class="col-auto">
                            <q-btn color="grey-7" round flat icon="more_vert">
                                <q-menu cover auto-close>
                                    <q-list>
                                        <q-item clickable>
                                            <q-item-section>Remove Card</q-item-section>
                                        </q-item>
                                        <q-item clickable>
                                            <q-item-section>Send Feedback</q-item-section>
                                        </q-item>
                                        <q-item clickable>
                                            <q-item-section>Share</q-item-section>
                                        </q-item>
                                    </q-list>
                                </q-menu>
                            </q-btn>
                        </div>
                    </div>
                </q-card-section>
                <q-card-section>
                    {{ lorem }}
                </q-card-section>

                <q-separator />

                <q-card-actions>
                    <q-btn flat>Action 1</q-btn>
                    <q-btn flat>Action 2</q-btn>
                </q-card-actions>
            </q-card>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    title: {
      type: String,
      required: true
    },
    caption: {
      type: String,
      default: ''
    },
    link: {
      type: String,
      default: '#'
    },
    icon: {
      type: String,
      default: ''
    }
  },
  data () {
    return {
      lorem: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
      dataGrafico: 'dia'
    }
  }
}
</script>
