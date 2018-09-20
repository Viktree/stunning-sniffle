<template>
  <div class="main-wrapper">

    <nav class="navbar navbar-expand-lg navbar-dark bg-primary fixed-top" id="sideNav">
      <a class="navbar-brand js-scroll-trigger" href="#about">
        <span class="d-block d-lg-none">Start Bootstrap</span>
        <span class="d-none d-lg-block">
          <img class="img-fluid img-profile rounded-circle mx-auto mb-2" src="./assets/profile.jpg" alt="">
        </span>
      </a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#about">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#experience">Experience</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#education">Education</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#skills">Skills</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#interests">Interests</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#awards">Awards</a>
          </li>
        </ul>
      </div>
    </nav>

    <full-page class="container-fluid p-0" ref="fullpage" :options="options">

      <about></about>

      <section class="section p-3 p-lg-5 d-flex flex-column" id="experience">
        <div class="my-auto">
          <h2 class="mb-5">Experience</h2>

          <div class="resume-item d-flex flex-column flex-md-row mb-5" v-for="job in experience" :key="job.description">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">{{ job.position }}</h3>
              <div class="subheading mb-3">{{ job.company }}</div>
              <p>{{ job.description }}</p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">{{ job.startDate }} - {{ job.endDate }}</span>
            </div>
          </div>

        </div>

      </section>

      <section class="section p-3 p-lg-5 d-flex flex-column" id="education">
        <div class="my-auto">
          <h2 class="mb-5">Education</h2>

          <div class="resume-item d-flex flex-column flex-md-row mb-5">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">University of Colorado Boulder</h3>
              <div class="subheading mb-3">Bachelor of Science</div>
              <div>Computer Science - Web Development Track</div>
              <p>GPA: 3.23</p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">August 2006 - May 2010</span>
            </div>
          </div>

          <div class="resume-item d-flex flex-column flex-md-row">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">James Buchanan High School</h3>
              <div class="subheading mb-3">Technology Magnet Program</div>
              <p>GPA: 3.56</p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">August 2002 - May 2006</span>
            </div>
          </div>

        </div>
      </section>

      <section class="section p-3 p-lg-5 d-flex flex-column" id="skills">
        <div class="my-auto">
          <h2 class="mb-5">Skills</h2>

          <div class="subheading mb-3">Programming Languages &amp; Tools</div>
          <ul class="list-inline list-icons">
            <li class="list-inline-item">
              <i class="devicons devicons-html5"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-css3"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-javascript"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-jquery"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-sass"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-less"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-bootstrap"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-wordpress"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-grunt"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-gulp"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-npm"></i>
            </li>
          </ul>

          <div class="subheading mb-3">Workflow</div>
          <ul class="fa-ul mb-0">
            <li>
              <i class="fa-li fa fa-check"></i>
              Mobile-First Responsive Design</li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Cross Browser Testing &amp; Debugging</li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Cross Functional Teams</li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Agile Development &amp; Scrum</li>
          </ul>
        </div>
      </section>

      <section class="section p-3 p-lg-5 d-flex flex-column" id="interests">
        <div class="my-auto">
          <h2 class="mb-5">Interests</h2>
          <p>Apart from being a web developer, I enjoy most of my time being outdoors. In the winter, I am an avid skiier and novice ice climber. During the warmer months here in Colorado, I enjoy mountain biking, free climbing, and kayaking.</p>
          <p class="mb-0">When forced indoors, I follow a number of sci-fi and fantasy genre movies and television shows, I am an aspiring chef, and I spend a large amount of my free time exploring the latest technolgy advancements in the front-end web development world.</p>
        </div>
      </section>

      <section class="section p-3 p-lg-5 d-flex flex-column" id="awards">
        <div class="my-auto">
          <h2 class="mb-5">Awards &amp; Certifications</h2>
          <ul class="fa-ul mb-0">
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              Google Analytics Certified Developer</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              Mobile Web Specialist - Google Certification</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              <sup>st</sup>
              Place - University of Colorado Boulder - Emerging Tech Competition 2009</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              <sup>st</sup>
              Place - University of Colorado Boulder - Adobe Creative Jam 2008 (UI Design Category)</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              <sup>nd</sup>
              Place - University of Colorado Boulder - Emerging Tech Competition 2008</li>
            <li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              <sup>st</sup>
              Place - James Buchanan High School - Hackathon 2006</li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              <sup>rd</sup>
              Place - James Buchanan High School - Hackathon 2005</li>
          </ul>
        </div>
      </section>

    </full-page>

  </div>
</template>

<script>
import About from './components/About.vue'

export default {
  data: () => ({
    experience: [
      {
        position: 'Senior Web Developer',
        company: 'Intelitec Solutions',
        description:
          'Bring to the table win-win survival strategies to ensure proactive domination. At the end of the day, going forward, a new normal that has evolved from generation X is on the runway heading towards a streamlined cloud solution. User generated content in real-time will have multiple touchpoints for offshoring.',
        startDate: 'March 2013',
        endDate: 'Present'
      },
      {
        position: 'Web Developer',
        company: 'Intelitec Solutions',
        description:
        'Capitalize on low hanging fruit to identify a ballpark value added activity to beta test. Override the digital divide with additional clickthroughs from DevOps. Nanotechnology immersion along the information highway will close the loop on focusing solely on the bottom line.',
        startDate: 'December 2011',
        endDate: 'March 2013'
      },
      {
        position: 'Junior Web Designer',
        company: 'Shout! Media Productions',
        description:
        'Podcasting operational change management inside of workflows to establish a framework. Taking seamless key performance indicators offline to maximise the long tail. Keeping your eye on the ball while performing a deep dive on the start-up mentality to derive convergence on cross-platform integration.',
        startDate: 'July 2010',
        endDate: 'December 2011'
      },
      {
        position: 'Web Design Intern',
        company: 'Shout! Media Productions',
        description:
        'Collaboratively administrate empowered markets via plug-and-play networks. Dynamically procrastinate B2C users after installed base benefits. Dramatically visualize customer directed convergence without revolutionary ROI.',
        startDate: 'September 2008',
        endDate: 'June 2010'
      }
    ]
  }),
  components: {
    About
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

#sideNav .navbar-nav .nav-item .nav-link
  font-weight: 600
  text-transform: uppercase

@media (min-width: 992px)
  #sideNav
    text-align: center
    position: fixed
    top: 0
    left: 0
    display: flex
    flex-direction: column
    width: 17rem
    height: 100vh

  #sideNav .navbar-brand
    display: flex
    margin: auto auto 0
    padding: 0.5rem

  #sideNav .navbar-brand .img-profile
    max-width: 10rem
    max-height: 10rem
    border: 0.5rem solid rgba(255, 255, 255, 0.2)

  #sideNav .navbar-collapse
    display: flex
    align-items: flex-start
    flex-grow: 0
    width: 100%
    margin-bottom: auto

  #sideNav .navbar-collapse .navbar-nav
    flex-direction: column
    width: 100%

  #sideNav .navbar-collapse .navbar-nav .nav-item
    display: block

  #sideNav .navbar-collapse .navbar-nav .nav-item .nav-link
    display: block

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
