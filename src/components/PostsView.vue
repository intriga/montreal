<template>
  <div class="col-md-8 grid-sidebar" id="content">
    <!-- start grid sidebar -->
    <div
      class="jelly_homepage_builder jl_nonav_margin homepage_builder_3grid_post jl_fontsize22 jl_cus_grid2 colstyle1"
    >
      <div class="jl_wrapper_row jl-post-block-416765">
        <div class="row">
          <div class="box blog_grid_post_style jl_row_1" v-for="value in posts" :key="value">
            <div class="jl_grid_box_wrapper">
              <div class="image-post-thumb">
                <a
                  href="#"
                  class="link_image featured-thumbnail"
                  title="Every photographer needs to shoot this photo"
                >
                  <img
                    width="780"
                    height="450"
                    :src="value.image"
                    class="attachment-disto_large_feature_image size-disto_large_feature_image wp-post-image"
                    alt=""
                  />
                  <div class="background_over_image"></div>
                </a>
                <span class="meta-category-small"
                  ><a class="post-category-color-text" style="background: #6b34ba" href="#"
                    >Gaming</a
                  ></span
                >
                <span class="jl_post_type_icon"><i class="la la-volume-up"></i></span>
              </div>
              <div class="post-entry-content">
                <h3 class="image-post-title">
                  <a :href="'/post/' + value.slug">{{ value.title }}</a>
                </h3>
                <span class="jl_post_meta">
                  <span class="jl_author_img_w">
                    <img
                      src="../../public/img/favicon.jpg"
                      width="30"
                      height="30"
                      class="avatar avatar-30 wp-user-avatar wp-user-avatar-30 alignnone photo"
                    />
                    <a href="#" rel="author">Anna Nikova</a>
                  </span>
                  <span class="post-date"
                    ><i class="fa fa-clock-o"></i>{{ format_date(value.created_at) }}</span
                  >
                </span>
              </div>
            </div>
          </div>

          <div class="clear_line_3col_home"></div>
          <div class="jl-loadmore-btn-w">
            <a href="#" class="jl_btn_load">Load more</a>
          </div>
        </div>
      </div>
    </div>
    <!-- end grid sidebar -->
  </div>
</template>

<script>
import axios from 'axios'
import moment from 'moment'

export default {
  data() {
    return {
      posts: []
    }
  },

  mounted() {
    this.getPosts()
  },

  methods: {
    getPosts() {
      axios.get('http://127.0.0.1:8000/api/posts').then((res) => {
        this.posts = res.data
        console.log(this.posts)
      })
    },

    format_date(value) {
      if (value) {
        return moment(String(value)).format('DD/MM/YYYY')
      }
    }
  }
}
</script>
