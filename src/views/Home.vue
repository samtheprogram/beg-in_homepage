<template lang="pug">
main#home
  .header-shadow-cover
  .hero
    .frow-container.height-100
      .frow.column-start.justify-center.height-100
        .hero-content
          h2
            | We solve your software challenges.
          h5
            | Part talent agency, part product agency. Begin delivers reliable technology solutions for your business.
  .were-good.site-section
    .frow-container.height-100
      .frow.centered-column.height-100
        .title
          h2
            | Start Here
          h5
            | Work with a team that allows you to do what you do best: run your business.
      .service-box-parent
        .frow.gutters
          .col-md-4-10
            .service-box
              .frow.column-center
                cbox1Svg
                h5
                  | Product Development
                p
                  | Your idea, brought to life. We like to build entire technology platforms from scratch. They’re fast, secure, and highly scalable.
          .col-md-1-10
            .frow.centered
               span.plus
                | &
          .col-md-4-10
            .service-box
              .frow.column-center
                brainSvg
                h5
                  | Technology Consulting
                p
                  | Tap into Beg.in's extensive tech experience to plan your next product launch.
          .frow
            router-link.begin-button(to="contact", title="Contact", type="button") Start a project
  .team.site-section
    .frow-container.height-100
      .frow.row-start
        .col-md-2-5
          .frow.centered-column.height-100
            .title
              h2
                | Meet our team
        .col-md-3-5
          .team-box-parent
            .frow.gutters
              .col-md-1-6.col-xs-1-3(v-for="member in team")
                .team-box
                  .frow.column-center
                    img(:src="member.img")
                    h6
                      | {{member.firstName}}
      .frow
        router-link.begin-button(to="team", title="Our Team", type="button") Learn More
  .slate.site-section
    .frow-container.height-100
      .frow.centered-column.height-100
        .title
          .frow.row-center
            h5
              | Modern web toolkits, powering your idea.
            .frow
              .col-md-1-1
                p
                  | Our battle-tested product development tools ensure you're not paying for us to reinvent the wheel.
                  br
                  | Your plumber should show up to the job with her tools ready-to-go.
        .frow.gutters
          .col-md-1-1
            .service-box
              .frow.column-center
          .col-md-1-4.col-sm-1-2
            .service-box
              .frow.column-center
                craneSvg
                h5
                  | Scalable
                p
                  | Never worry about your big day on Oprah.
          .col-md-1-4.col-sm-1-2
            .service-box
              .frow.column-center
                vaultSvg
                h5
                  | Secure
                p
                  | Get access to HIPAA compliant security.
          .col-md-1-4.col-sm-1-2
            .service-box
              .frow.column-center
                multiSvg
                h5
                  | Versatile
                p
                  | Push notifications, user profiles, it's all there.
                  // br
                  // |It's all there.
          .col-md-1-4.col-sm-1-2
            .service-box
              .frow.column-center
                robotSvg
                h5
                  | Efficient
                p
                  | It's fast. Really fast.

  ContactFooter
</template>
<script>
import { team } from '../data/team';
import cubeSvg from '@/assets/svgs/cube.svg';
import statsSvg from '@/assets/svgs/stats.svg';
import slateSvg from '@/assets/svgs/slate.svg';
import vaultSvg from '@/assets/svgs/vault.svg';
import multiSvg from '@/assets/svgs/multi.svg';
import craneSvg from '@/assets/svgs/crane.svg';
import robotSvg from '@/assets/svgs/robot.svg';
import cbox1Svg from '@/assets/svgs/creative-box.svg';
import cbox2Svg from '@/assets/svgs/creative-box-2.svg';
import brainSvg from '@/assets/svgs/brainstorm.svg';

import ContactFooter from '@/components/ContactFooter';
export default {
  components: {
    ContactFooter,
    cubeSvg,
    statsSvg,
    slateSvg,
    vaultSvg,
    multiSvg,
    craneSvg,
    robotSvg,
    cbox1Svg,
    cbox2Svg,
    brainSvg,
  },
  data() {
    return {
      team,
    };
  },
};
</script>
<style lang="sass" scoped>
@import @/assets/styles/variables.sass

.header-shadow-cover
  top: $header-height - 2px
  position: absolute
  width: 100%
  background-color: $primary-color
  height: 13px
  z-index: 3

.hero
  height: 700px
  background-color: $primary-color
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='100%25' height='100%25' viewBox='0 0 100 60'%3E%3Cg %3E%3Crect fill='%2312d8b7' width='11' height='11'/%3E%3Crect fill='%2314d7b6' x='10' width='11' height='11'/%3E%3Crect fill='%2316d6b6' y='10' width='11' height='11'/%3E%3Crect fill='%2318d5b5' x='20' width='11' height='11'/%3E%3Crect fill='%2319d4b5' x='10' y='10' width='11' height='11'/%3E%3Crect fill='%231bd3b4' y='20' width='11' height='11'/%3E%3Crect fill='%231cd2b3' x='30' width='11' height='11'/%3E%3Crect fill='%231ed1b3' x='20' y='10' width='11' height='11'/%3E%3Crect fill='%231fd0b2' x='10' y='20' width='11' height='11'/%3E%3Crect fill='%2320cfb2' y='30' width='11' height='11'/%3E%3Crect fill='%2321ceb1' x='40' width='11' height='11'/%3E%3Crect fill='%2323cdb0' x='30' y='10' width='11' height='11'/%3E%3Crect fill='%2324ccb0' x='20' y='20' width='11' height='11'/%3E%3Crect fill='%2325cbaf' x='10' y='30' width='11' height='11'/%3E%3Crect fill='%2326caaf' y='40' width='11' height='11'/%3E%3Crect fill='%2327c9ae' x='50' width='11' height='11'/%3E%3Crect fill='%2328c7ad' x='40' y='10' width='11' height='11'/%3E%3Crect fill='%2329c6ad' x='30' y='20' width='11' height='11'/%3E%3Crect fill='%232ac5ac' x='20' y='30' width='11' height='11'/%3E%3Crect fill='%232bc4ab' x='10' y='40' width='11' height='11'/%3E%3Crect fill='%232cc3ab' y='50' width='11' height='11'/%3E%3Crect fill='%232dc2aa' x='60' width='11' height='11'/%3E%3Crect fill='%232dc1aa' x='50' y='10' width='11' height='11'/%3E%3Crect fill='%232ec0a9' x='40' y='20' width='11' height='11'/%3E%3Crect fill='%232fbfa8' x='30' y='30' width='11' height='11'/%3E%3Crect fill='%2330bea8' x='20' y='40' width='11' height='11'/%3E%3Crect fill='%2331bda7' x='10' y='50' width='11' height='11'/%3E%3Crect fill='%2331bca6' x='70' width='11' height='11'/%3E%3Crect fill='%2332bba6' x='60' y='10' width='11' height='11'/%3E%3Crect fill='%2333baa5' x='50' y='20' width='11' height='11'/%3E%3Crect fill='%2334b9a4' x='40' y='30' width='11' height='11'/%3E%3Crect fill='%2334b8a4' x='30' y='40' width='11' height='11'/%3E%3Crect fill='%2335b7a3' x='20' y='50' width='11' height='11'/%3E%3Crect fill='%2336b6a2' x='80' width='11' height='11'/%3E%3Crect fill='%2336b5a2' x='70' y='10' width='11' height='11'/%3E%3Crect fill='%2337b4a1' x='60' y='20' width='11' height='11'/%3E%3Crect fill='%2337b3a0' x='50' y='30' width='11' height='11'/%3E%3Crect fill='%2338b2a0' x='40' y='40' width='11' height='11'/%3E%3Crect fill='%2339b19f' x='30' y='50' width='11' height='11'/%3E%3Crect fill='%2339b09e' x='90' width='11' height='11'/%3E%3Crect fill='%233aaf9e' x='80' y='10' width='11' height='11'/%3E%3Crect fill='%233aae9d' x='70' y='20' width='11' height='11'/%3E%3Crect fill='%233bad9c' x='60' y='30' width='11' height='11'/%3E%3Crect fill='%233cac9b' x='50' y='40' width='11' height='11'/%3E%3Crect fill='%233cab9b' x='40' y='50' width='11' height='11'/%3E%3Crect fill='%233daa9a' x='90' y='10' width='11' height='11'/%3E%3Crect fill='%233da999' x='80' y='20' width='11' height='11'/%3E%3Crect fill='%233ea899' x='70' y='30' width='11' height='11'/%3E%3Crect fill='%233ea798' x='60' y='40' width='11' height='11'/%3E%3Crect fill='%233fa697' x='50' y='50' width='11' height='11'/%3E%3Crect fill='%233fa597' x='90' y='20' width='11' height='11'/%3E%3Crect fill='%2340a496' x='80' y='30' width='11' height='11'/%3E%3Crect fill='%2340a395' x='70' y='40' width='11' height='11'/%3E%3Crect fill='%2340a294' x='60' y='50' width='11' height='11'/%3E%3Crect fill='%2341a194' x='90' y='30' width='11' height='11'/%3E%3Crect fill='%2341a093' x='80' y='40' width='11' height='11'/%3E%3Crect fill='%23429f92' x='70' y='50' width='11' height='11'/%3E%3Crect fill='%23429e91' x='90' y='40' width='11' height='11'/%3E%3Crect fill='%23439d91' x='80' y='50' width='11' height='11'/%3E%3Crect fill='%23439c90' x='90' y='50' width='11' height='11'/%3E%3C/g%3E%3C/svg%3E")
  background-attachment: fixed
  background-size: cover
  /* background by SVGBackgrounds.com */
  color: #fff
  text-shadow: 1px 1px 1px #777

.hero-content
  max-width: 830px

.were-good
  text-align: center
  background-color: $light-background

  .plus
    font-size: 82px
    font-weight: 500
    color: $primary-color
    margin: 34px 0 44px
    display: none

#home
  p
    font-size: 19px
    line-height: 28px

  .service-box
    svg
      width: 138px
      height: auto
      margin-bottom: 15px

.team.site-section .title
  text-align: left

.service-box
  padding: 0 32px

  p
    margin: 10px 0 28px 0
    text-align: center

  h5
    font-weight: 500

.team-box
  img
    width: 140px
    border-radius: 20%
    margin-bottom: 11px

.slate
  background-color: $light-background

  .slate-logo
    svg
      margin-right: 8px
      margin-bottom: 0
      width: 38px

@media screen and (max-width: 767px)
  .team-box
    img
      width: 100px
    h6
      margin-bottom: 8px
</style>
