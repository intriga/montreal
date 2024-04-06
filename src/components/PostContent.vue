<template>
  <div>
    <div class="jl_single_style1">
      <div class="single_content_header jl_single_feature_above">
        <div class="image-post-thumb jlsingle-title-above">
          <img
            width="1000"
            height="667"
            :src="model.post.image"
            class="attachment-disto_justify_feature size-disto_justify_feature wp-post-image"
            alt=""
          />
        </div>
      </div>
      <div class="single_post_entry_content single_bellow_left_align">
        <span class="meta-category-small single_meta_category"
          ><a class="post-category-color-text" style="background: #d1783c" href="#">Crazy</a></span
        >
        <h1 class="single_post_title_main">{{ model.post.title }}</h1>
        <span class="single-post-meta-wrapper"
          ><span class="post-author"
            ><span
              ><img
                src="../../public/img/favicon.jpg"
                width="50"
                height="50"
                alt="Anna Nikova"
                class="avatar avatar-50 wp-user-avatar wp-user-avatar-50 alignnone photo"
              /><a href="#" title="Posts by Anna Nikova" rel="author">Anna Nikova</a></span
            ></span
          ><span class="post-date updated"
            ><i class="fa fa-clock-o"></i>{{ format_date(model.post.created_at) }}</span
          ><span class="meta-comment"><i class="fa fa-comment"></i><a href="#">0 Comment</a></span
          ><a href="#" class="jm-post-like" data-post_id="2800" title="Like"
            ><i class="fa fa-heart-o"></i>1</a
          ><span class="view_options"><i class="fa fa-eye"></i>3.6k</span></span
        >
      </div>
    </div>
    <div class="post_content">
      <p>{{ model.post.content }}<span id="more-2800"></span></p>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import moment from 'moment'

export default {
  data() {
    return {
      capturedSlug: null,
      model: {
        post: {
          title: '',
          image: '',
          content: '',
          created_at: ''
        }
      }
    }
  },

  mounted() {
    this.getPost()
  },

  methods: {
    getPost() {
      const urlFull = window.location.href
      const urlParts = urlFull.split('/')

      const slug = urlParts[urlParts.length - 1]
      //console.log(slug);

      axios.get(`http://127.0.0.1:8000/api/post/${slug}`).then((res) => {
        this.post = res.data
        console.log(this.post)

        this.model.post = {
          title: res.data.title,
          image: res.data.image,
          content: res.data.content,
          created_at: res.data.created_at
        }
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
