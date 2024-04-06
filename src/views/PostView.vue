<template>
  <div class="options_layout_wrapper jl_radius jl_none_box_styles jl_border_radiuss">
    <div class="options_layout_container full_layout_enable_front">
      <div class="mobile_menu_overlay"></div>
      <!-- begin content -->
      <section id="content_main" class="clearfix jl_spost">
        <div class="container">
          <div class="row main_content">
            <div class="col-md-8 loop-large-post" id="content">
              <div class="widget_container content_page">
                <!-- start post -->
                <div
                  class="post-2800 post type-post status-publish format-standard has-post-thumbnail hentry category-crazy tag-food tag-inspiration"
                  id="post-2800"
                >
                  <div class="single_section_content box blog_large_post_style">
                    <!-- start div -->
                    <PostContent />
                    <!-- end div -->
                    <div class="clearfix"></div>
                    <div class="single_tag_share">
                      <div class="tag-cat">
                        <ul class="single_post_tag_layout">
                          <li><a href="#" rel="tag">food</a></li>
                          <li><a href="#" rel="tag">inspiration</a></li>
                        </ul>
                      </div>

                      <div class="single_post_share_icons">
                        Share<i class="fa fa-share-alt"></i>
                      </div>
                    </div>
                    <div class="single_post_share_wrapper">
                      <div class="single_post_share_icons social_popup_close">
                        <i class="fa fa-close"></i>
                      </div>
                      <ul class="single_post_share_icon_post">
                        <li class="single_post_share_facebook">
                          <a href="#" target="_blank"><i class="fa fa-facebook"></i></a>
                        </li>
                        <li class="single_post_share_twitter">
                          <a href="#" target="_blank"><i class="fa fa-twitter"></i></a>
                        </li>
                        <li class="single_post_share_pinterest">
                          <a href="#" target="_blank"><i class="fa fa-pinterest"></i></a>
                        </li>
                        <li class="single_post_share_linkedin">
                          <a href="#" target="_blank"><i class="fa fa-linkedin"></i></a>
                        </li>
                        <li class="single_post_share_ftumblr">
                          <a href="#" target="_blank"><i class="fa fa-tumblr"></i></a>
                        </li>
                      </ul>
                    </div>

                    <div class="postnav_left">
                      <div class="single_post_arrow_content">
                        <a href="#" id="prepost">
                          The best inspiration painting and fast in the world
                          <span class="jl_post_nav_left"> Previous post</span></a
                        >
                      </div>
                    </div>

                    <div class="postnav_right">
                      <div class="single_post_arrow_content">
                        <a href="#" id="nextpost">
                          Sometime reading can me you feel relaxed
                          <span class="jl_post_nav_left"> Next post</span></a
                        >
                      </div>
                    </div>

                    <!-- author-info -->
                    <AuthorInfo />
                    <!-- /author-info -->

                    <!-- related-post -->
                    <RelatedPost />
                    <!-- /related-post -->
                  </div>
                </div>
                <!-- end post -->
                <div class="brack_space"></div>
              </div>
            </div>

            <!-- /sidebar -->
            <SidebarView />
            <!-- /sidebar -->
          </div>
        </div>
      </section>
      <!-- end content -->
      <!-- Start footer -->
      <FooterView />
      <!-- End footer -->
    </div>
  </div>
</template>

<script setup>
import PostContent from '../components/PostContent.vue'
import SidebarView from '../components/SidebarView.vue'
import AuthorInfo from '../components/AuthorInfo.vue'
import RelatedPost from '../components/RelatedPost.vue'
import FooterView from '../components/FooterView.vue'
</script>
