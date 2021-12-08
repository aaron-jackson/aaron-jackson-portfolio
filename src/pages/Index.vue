<template>
  <Layout>
    <div class="hero container-inner mx-auto flex flex-col sm:flex-row justify-between py-16 mt-8">
      <div class="text-4xl font-bold w-full sm:w-3/5 text-center sm:text-left">
        <div class="leading-tight">Aaron Jackson</div>
        <div class="text-green-700 leading-tight">Front End Developer</div>
      </div>
      <div class="mt-8 sm:mt-0">
        <g-image src="../../static/developer.svg" alt="hero" class="mx-auto sm:mx-0" />
      </div>
    </div> <!-- end hero -->

    <div class="container-inner mx-auto">
      <p class="text-lg sm:text-xl">Hi, welcome to my site! I'm a freelance developer that builds interactive and user-friendly websites. Let's work together and make your ideas come alive on the internet. Drop me a <a href="/#contact" v-scroll-to="{ el: '#contact', offset: -25 }">message</a>.</p>

      <div class="flex justify-between items-center py-6">
        <div class="w-full sm:w-1/2 px-8 py-8 sm:py-0">
          <g-image src="../../static/undraw_web_developer_re_h7ie.svg" alt="Programmer" />
        </div>
        <div class="w-1/2 px-8 hidden sm:flex justify-end">
          <g-image src="../../static/browser-web-development.svg" alt="Browser" />
        </div>
      </div>
    </div>

    <div class="overflow-x-hidden">
      <div id="projects" style="position: relative; top: -40px; left: 0"/>
      <div class="projects container-inner mx-auto text-xl border-t border-gray-500 border-b py-16 mb-16 relative">
        <h2 class="font-bold mb-6">Here are some recent projects I've worked on:</h2>

        <div class="absolute right-0" style="top: 50px; transform: translate(100%) rotate(180deg)">
          <svg width="170px" height="170px"><use xlink:href="#dots-triangle" /></svg>
        </div>

          <div class="grid grid-cols-2 gap-8">
            <div class="transform transition duration-500 hover:scale-110">
              <a href="https://www.chapmancommunities.org/" target="_blank"><img class="rounded shadow-md" src="chapmancommunities.png" alt=""></a>
              <h3>Chapman Foundation for<br> Caring Communities</h3>
            </div>
            <div class="transform transition duration-500 hover:scale-110">
              <a href="https://www.northernengraving.com/" target="_blank"><img class="rounded shadow-md" src="northern-engraving.png" alt=""></a>
              <h3>Northern Engraving</h3>
            </div>
            <div class="transform transition duration-500 hover:scale-110"> 
              <a href="https://www.bwflexiblesystems.com/" target="_blank"><img class="rounded shadow-md" src="bwflexible-systems.png" alt=""></a>
              <h3>Flexible Systems</h3>
            </div>
            <div class="transform transition duration-500 hover:scale-110">
              <a href="https://www.pcmc.com/" target="_blank"><img class="rounded shadow-md" src="pcmc.png" alt=""></a>
              <h3>Paper Converting Machine Company</h3>
            </div>
          </div>

      </div> <!-- end projects -->
    </div>

    <div class="overflow-x-hidden border-gray-200 border-b">
      <div id="about" style="position: relative; top: -40px; left: 0"/>
      <div class="get-to-know-me container-inner mx-auto text-xl pb-16 relative">
        <h2 class="font-bold mb-6">Get to know me:</h2>

        <div class="absolute left-0" style="top: 50px; transform: translateX(-100%)">
          <svg width="170px" height="170px"><use xlink:href="#dots-triangle" /></svg>
        </div>

        <div class="flex flex-col sm:flex-row justify-between items-center mb-16">
          <div><g-image src="../../static/my-pic.jpeg" alt="avatar" class="w-32 h-32 rounded-full mb-8 lg:mb-0" /></div>
          <div class="flex-1 text-lg sm:text-xl ml-6">I'm a developer based out of St. Charles, MO. I enjoy solving problems and turning design concepts into pixel perfect websites. When I'm not writing code. I'm a husband and a dad to two beautiful girls.</div>
        </div>

        <div class="">
          <h3 class="font-bold">My Skills</h3>
          <div class="skills-container">
            <div class="p-10 flex flex-col space-y-3">
              <h4>CSS</h4>
              <div class="relative w-full sm:w-1/2 bg-gray-200 rounded">
                <div style="width: 95%" class="absolute top-0 h-4 rounded shim-green"></div>
              </div>
              <h4>Semantic HTML</h4>
              <div class="relative w-full sm:w-1/2 bg-gray-200 rounded">
                <div style="width: 95%" class="absolute top-0 h-4 rounded shim-green"></div>
              </div>
              <h4>Javascript</h4>
              <div class="relative w-full sm:w-1/2 bg-gray-200 rounded">
                <div style="width: 77%" class="absolute top-0 h-4 rounded shim-green"></div>
              </div>
              <h4>PHP</h4>
              <div class="relative w-full sm:w-1/2 bg-gray-200 rounded">
                <div style="width: 80%" class="absolute top-0 h-4 rounded shim-green"></div>
              </div>
               <h4>WordPress</h4>
              <div class="relative w-full sm:w-1/2 bg-gray-200 rounded">
                <div style="width: 80%" class="absolute top-0 h-4 rounded shim-green"></div>
              </div>
              <h4>SEO</h4>
              <div class="relative w-full sm:w-1/2 bg-gray-200 rounded">
                <div style="width: 60%" class="absolute top-0 h-4 rounded shim-green"></div>
              </div>
            </div>
          </div>
        </div>
      </div> <!-- end get-to-know me -->
    </div>

    <div class="overflow-x-hidden">
      <div id="contact" style="position: relative; top: -40px; left: 0"/>
      <div class="contact-me bg-background-secondary pt-16">
        <div class="container-inner mx-auto text-xl pb-4 relative">
          <h2 class="font-bold mb-6">Contact me:</h2>

          <div class="absolute right-0 top-0" style="transform: translate(100%) rotate(180deg)">
            <svg width="170px" height="170px"><use xlink:href="#dots-triangle" /></svg>
          </div>

          <p class="mb-12">If you're looking to work together, talk about past projects or chat over coffee. Get in touch.</p>

          <div class="text-lg sm:text-lg mb-16">
            <form data-netlify="true" name="contact" method="POST" class="mb-12" id="contact-form" content-type="application/x-www-form-urlencoded">
              <div class="flex flex-wrap mb-6 -mx-4">
                  <div class="w-full md:w-1/2 mb-6 md:mb-0 px-4">
                      <label class="block mb-2 text-copy-primary" for="name">
                          Name
                      </label>

                      <input type="text" name="name" id="name" placeholder="Name" class="block w-full bg-background-form border border-border-color-primary shadow rounded outline-none focus:border-green-700 mb-2 p-4" required>
                  </div>

                  <div class="w-full px-4 md:w-1/2">
                      <label class="block text-copy-primary mb-2" for="email">
                          Email Address
                      </label>

                      <input type="email" name="email" id="email" placeholder="email@example.com"  class="block w-full bg-background-form border border-border-color-primary shadow rounded outline-none focus:border-green-700 mb-2 p-4" required>
                  </div>
              </div>

              <div class="w-full mb-12">
                  <label class="block text-copy-primary mb-2" for="message">
                      Message
                  </label>

                  <textarea id="message" rows="5" name="message" class="block w-full bg-background-form border border-border-color-primary shadow rounded outline-none appearance-none focus:border-green-700 mb-2 px-4 py-4" placeholder="Enter your message here." required></textarea>
              </div>

              <div class="flex justify-end w-full">
                  <input type="submit" value="Submit" class="block bg-green-700 hover:bg-green-800 text-white text-sm font-semibold tracking-wide uppercase shadow rounded cursor-pointer px-6 py-3">
              </div>
          </form>
          </div>
        </div>
      </div> <!-- end contact-me -->
    </div>


  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Home'
  }
}
</script>
