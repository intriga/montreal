<template>
  <div>
    <div class="jl_home_bw">
      <div class="container">
        <div class="row">
          <!-- start slider -->
          <SliderView />
          <!-- end slider -->

          <div class="jl_home_section jl_home_slider">
            <div class="container">
              <div class="row">
                <PostsView />

                <!-- start sidebar -->
                <SidebarView />
                <!-- end sidebar -->
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- end content -->

    <!-- Start footer -->
    <FooterView />
  </div>
</template>

<script setup>
import SliderView from '../components/SliderView.vue'
import PostsView from '../components/PostsView.vue'
import SidebarView from '../components/SidebarView.vue'
import FooterView from '../components/FooterView.vue'
</script>
