<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>
<template>
  <div>
    <div class="options_layout_wrapper jl_radius jl_none_box_styles jl_border_radiuss">
      <div class="options_layout_container full_layout_enable_front">
        <!-- Start header -->
        <header
          class="header-wraper jl_header_magazine_style two_header_top_style header_layout_style3_custom jl_cusdate_head"
        >
          <div class="header_top_bar_wrapper">
            <div class="container">
              <div class="row">
                <div class="col-md-12">
                  <div class="menu-primary-container navigation_wrapper">
                    <ul id="jl_top_menu" class="jl_main_menu">
                      <li
                        class="menu-item menu-item-home current-menu-item page_item page-item-4212 current_page_item menu-item-4461"
                      >
                        <a href="#" aria-current="page">Home<span class="border-menu"></span></a>
                      </li>
                      <li class="menu-item menu-item-3602">
                        <a href="#">Member<span class="border-menu"></span></a>
                      </li>
                      <li class="menu-item menu-item-3606">
                        <a href="#">special offer<span class="border-menu"></span></a>
                      </li>
                      <li class="menu-item menu-item-3598">
                        <a href="#">Info!!<span class="border-menu"></span></a>
                      </li>
                    </ul>
                  </div>
                  <div class="jl_top_bar_right">
                    <span class="jl_current_title">Current Date:</span> 7 July, 2020
                  </div>
                </div>
              </div>
            </div>
          </div>
          <!-- Start Main menu -->
          <div class="jl_blank_nav"></div>
          <div id="menu_wrapper" class="menu_wrapper jl_menu_sticky jl_stick">
            <div class="container">
              <div class="row">
                <div class="main_menu col-md-12">
                  <div class="logo_small_wrapper_table">
                    <div class="logo_small_wrapper">
                      <!-- begin logo -->
                      <a class="logo_link" href="index.html">
                        <img src="../public/img/logo.png" alt="Just another WordPress site" />
                      </a>
                      <!-- end logo -->
                    </div>
                  </div>
                  <!-- main menu -->
                  <div class="menu-primary-container navigation_wrapper">
                    <ul id="mainmenu" class="jl_main_menu">
                      <li class="menu-item">
                        <RouterLink to="/">Home<span class="border-menu"></span></RouterLink>
                      </li>
                      <li class="menu-item">
                        <RouterLink to="/about"
                          >About Us<span class="border-menu"></span
                        ></RouterLink>
                      </li>
                      <li class="menu-item">
                        <RouterLink to="/contact"
                          >contact Us<span class="border-menu"></span
                        ></RouterLink>
                      </li>
                    </ul>
                  </div>
                  <!-- end main menu -->
                  <div class="search_header_menu">
                    <div class="menu_mobile_icons">
                      <i class="fa fa-bars"></i>
                    </div>
                    <div class="search_header_wrapper search_form_menu_personal_click">
                      <i class="fa fa-search"></i>
                    </div>
                    <div class="menu_mobile_share_wrapper">
                      <ul class="social_icon_header_top">
                        <li>
                          <a class="facebook" href="#" target="_blank"
                            ><i class="fa fa-facebook"></i
                          ></a>
                        </li>
                        <li>
                          <a class="google_plus" href="#" target="_blank"
                            ><i class="fa fa-google-plus"></i
                          ></a>
                        </li>
                        <li>
                          <a class="behance" href="#" target="_blank"
                            ><i class="fa fa-behance"></i
                          ></a>
                        </li>
                      </ul>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </header>
        <div id="content_nav" class="jl_mobile_nav_wrapper">
          <div id="nav" class="jl_mobile_nav_inner">
            <div class="menu_mobile_icons mobile_close_icons closed_menu">
              <span class="jl_close_wapper"
                ><span class="jl_close_1"></span><span class="jl_close_2"></span
              ></span>
            </div>
            <ul id="mobile_menu_slide" class="menu_moble_slide">
              <li class="menu-item">
                <RouterLink to="/">Home<span class="border-menu"></span></RouterLink>
              </li>
              <li class="menu-item">
                <RouterLink to="/about">About Us<span class="border-menu"></span></RouterLink>
              </li>
              <li class="menu-item">
                <RouterLink to="/contact">contact Us<span class="border-menu"></span></RouterLink>
              </li>
            </ul>
            <span class="jl_none_space"></span>
            <div id="disto_about_us_widget-2" class="widget jellywp_about_us_widget">
              <div class="widget_jl_wrapper about_widget_content">
                <div class="jellywp_about_us_widget_wrapper">
                  <div class="social_icons_widget">
                    <ul class="social-icons-list-widget icons_about_widget_display">
                      <li>
                        <a href="#" class="facebook" target="_blank"
                          ><i class="fa fa-facebook"></i
                        ></a>
                      </li>
                      <li>
                        <a href="#" class="google_plus" target="_blank"
                          ><i class="fa fa-google-plus"></i
                        ></a>
                      </li>
                      <li>
                        <a href="#" class="behance" target="_blank"
                          ><i class="fa fa-behance"></i
                        ></a>
                      </li>
                      <li>
                        <a href="#" class="vimeo" target="_blank"
                          ><i class="fa fa-vimeo-square"></i
                        ></a>
                      </li>
                      <li>
                        <a href="#" class="youtube" target="_blank"
                          ><i class="fa fa-youtube"></i
                        ></a>
                      </li>
                    </ul>
                  </div>
                </div>
                <span class="jl_none_space"></span>
              </div>
            </div>
          </div>
        </div>
        <div class="search_form_menu_personal">
          <div class="menu_mobile_large_close">
            <span class="jl_close_wapper search_form_menu_personal_click"
              ><span class="jl_close_1"></span><span class="jl_close_2"></span
            ></span>
          </div>
          <form method="get" class="searchform_theme" action="#">
            <input type="text" placeholder="Search..." value="" name="s" class="search_btn" />
            <button type="submit" class="button">
              <i class="fa fa-search"></i>
            </button>
          </form>
        </div>
        <div class="mobile_menu_overlay"></div>
        <!-- end header -->

        <RouterView />

        <!-- End footer -->
      </div>
    </div>
    <div id="go-top">
      <a href="#go-top"><i class="fa fa-angle-up"></i></a>
    </div>
  </div>
</template>
