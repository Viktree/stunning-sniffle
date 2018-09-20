<template lang='pug'>
  section.section.p-3.p-lg-5.d-flex.d-column#about
    .my-auto
      h1.mb-0 {{ name }}
        span.text-primary {{ surname }}
      div.subheading mb-5" {{ address }}
        a(href="mailto:name@email.com") {{ email }}
      p.mb-5 {{ aboutMe }}
      ul.list-inline.list-social-icons.mb-0
        each site in ['facebook', 'twitter', 'linkedin', 'github']
          li.list-inline-item
            a(href='#')
              span.fa-stack-lg
                i.fa.fa-circle.fa-stack-2x
                i.fa(class= "fa-" + site).fa-stack-1x.fa-inverse
</template>

<script>
export default {
  data () {
    return {
      title: 'My portfolio',
      name: 'CLARENCE',
      surname: 'TAYLOR',
      address: '3542 Berry Street · Cheyenne Wells, CO 80810 · (317) 585-8468 ·',
      email: 'name@email.com',
      aboutMe:
        'I am experienced in leveraging agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition.'
    }
  }
}
</script>

<style lang="stylus">
body
  font-family: 'Open Sans', serif
  padding-top: 54px
  color: #868e96

@media (min-width: 992px)
  body
    padding-top: 0
    padding-left: 17rem

h1,
h2,
h3,
h4,
h5,
h6
  font-family: 'Saira Extra Condensed', serif
  font-weight: 700
  text-transform: uppercase
  color: #343a40

h1
  font-size: 6rem;
  line-height: 5.5rem;

h2
  font-size: 3.5rem;

.subheading
  text-transform: uppercase;
  font-weight: 500;
  font-family: 'Saira Extra Condensed', serif;
  font-size: 1.35rem;

.list-social-icons a
  color: #495057

.list-social-icons a:hover
  color: #bd5d38

.list-social-icons a .fa-lg
  font-size: 1.75rem

.list-icons
  font-size: 3rem

.list-icons .list-inline-item i:hover
  color: #bd5d38

section.resume-section
  border-bottom: 1px solid #dee2e6
  padding-top: 5rem !important
  padding-bottom: 5rem !important

section.resume-section .resume-item .resume-date
  min-width: none

@media (min-width: 768px)
  section.resume-section
    min-height: 100vh

  section.resume-section .resume-item .resume-date
    min-width: 18rem

@media (min-width: 992px)
  section.resume-section
    padding-top: 3rem !important
    padding-bottom: 3rem !important

.bg-primary
  background-color: #bd5d38 !important

.text-primary
  color: #bd5d38 !important

a
  color: #bd5d38

a:hover,
a:focus,
a:active
  color: #824027

</style>
