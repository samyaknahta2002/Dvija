<script>
  import Carousel from 'svelte-carousel';
  import { browser } from '$app/environment';
  let index = 0;
  let arr = [
    {name: "Aman"},
    {name: "Hello"},
    {name: "World"},
  ]
</script>
<div class="bg-[#f5e6c8] w-full h-screen max-h-[945px]" style="font-family: TuskerGrotesk, sans-serif;background-image: url(grain.png);">
    <div class="navbar fixed top-0 w-full p-4 z-50">
        <div class="w-full rounded-md px-4 py-2 bg-white bg-opacity-80 backdrop-blur flex items-center justify-between">
            <img src="logo.png" alt="Logo" class="w-40 max-[1080px]:w-28">
            <div class="min-[900px]:hidden">
              <i class="fa fa-bars"></i>
              <div class="w-72 absolute top-10 right-4">
                <a href="/" class="px-2 py-1">Home</a>
                <a href="/" class="px-2 py-1">Global trends & SDG progress</a>
                <a href="/" class="px-2 py-1">Country profiles</a>
                <a href="/" class="px-2 py-1">Data centre & resources</a>
                <a href="/" class="px-2 py-1">Stories</a>
              </div>
            </div>
            <div class="flex items-center gap-4 uppercase max-[900px]:hidden max-[1080px]:gap-1 max-[1080px]:text-sm" style="font-family: Supreme, sans-serif;">
                <a href="/" class="px-2 py-1">Home</a>
                <a href="/" class="px-2 py-1">Global trends & SDG progress</a>
                <a href="/" class="px-2 py-1">Country profiles</a>
                <a href="/" class="px-2 py-1">Data centre & resources</a>
                <a href="/" class="px-2 py-1">Stories</a>
            </div>
        </div>
    </div>
    <div class="w-full h-screen flex max-h-[945px]">
        <div class="w-1/2 my-auto px-20 uppercase max-[450px]:w-full max-[450px]:px-10">
            <div class="text-lg tracking-wider mb-2">The Child Marriage Data Portal</div>
            <div class="text-6xl font-extrabold leading-tight">Every 3 seconds<br>a girl gets married<br>somewhere in the world</div>
        </div>
        <div class="w-1/2 my-auto px-20 max-[450px]:hidden">
          
        </div>
    </div>
</div>
<div class="bg-gray-100 w-full h-screen max-h-[945px]">
  <div class="w-full h-screen flex">
    <div class="w-1/3 my-auto px-20 max-[450px]:w-full max-[450px]:px-10">
        <div class="text-lg tracking-wider mb-1 uppercase" style="font-family: Satoshi, sans-serif;">Global trends & SDG progress</div>
        <div class="text-5xl font-extrabold leading-tight uppercase" style="font-family: TuskerGrotesk, sans-serif;">The global race to end child marriage</div>
        <div class="text-lg tracking-wider my-3" style="font-family: Satoshi, sans-serif;">Ending child marriage by 2030 is a target embedded in the Sustainable Development Goals. How far have countries progressed towards this target? And how much remains to be achieved?</div>
        <a href="/" class="flex gap-3 text-nowrap items-center mt-5">
          <i class="fa fa-arrow-right flex items-center justify-center w-12 h-12 rounded-full text-red-500 border border-red-500 text-2xl"></i>
          <span class="text-lg font-medium">Explore the trends</span>
        </a>
    </div>
    <div class="w-2/3 my-auto px-20 h-[65%] max-[450px]:hidden">
      <img src="" alt="img" class="border w-[75%] h-full m-auto">
    </div>
  </div>
</div>

<div class="bg-white w-full h-screen max-h-[945px] flex items-center relative">
  <div class="h-fit w-full">
    {#if browser}
      <Carousel autoplay autoplayDuration={3000} let:currentPageIndex let:pagesCount >
        {#each arr as arr}
          <div class="h-[80vh]">{arr.name} {index = currentPageIndex}</div>
        {/each}
      </Carousel>
    {/if}
  </div>
  <div class="absolute bottom-5 left-5 w-96 h-[46vh] min-h-[400px] bg-gray-500 rounded-lg max-[500px]:hidden" style="background-image: url(grain.png);">
    <div class="w-full h-full bg-gray-900 bg-opacity-80 rounded-lg">
      <span class="text-white text-xl">{index}</span>
    </div>
  </div>
</div>

<div class="bg-gray-100 w-full h-screen max-h-[945px]">
  <div class="w-full h-screen max-h-[945px] flex">
    <div class="w-1/3 my-auto px-20 max-[750px]:w-1/2 max-[500px]:w-full max-[500px]:px-10">
        <div class="text-lg tracking-wider mb-1 uppercase" style="font-family: Satoshi, sans-serif;">Country Profiles</div>
        <div class="text-5xl font-extrabold leading-tight uppercase" style="font-family: TuskerGrotesk, sans-serif;">Where does child marriage occur?</div>
        <div class="text-lg tracking-wider my-3" style="font-family: Satoshi, sans-serif;">Countries face different challenges in ending the practice and have varying rates of success. Explore the main indicators associated with child marriage in any country or region.</div>
        <a href="/" class="flex gap-3 text-nowrap items-center mt-5">
          <i class="fa fa-arrow-right flex items-center justify-center w-12 h-12 rounded-full text-red-500 border border-red-500 text-2xl"></i>
          <span class="text-lg font-medium">Check country status</span>
        </a>
    </div>
    <div class="w-2/3 my-auto px-20 h-[65%] max-[750px]:w-1/2 max-[500px]:hidden">
      <img src="" alt="img" class="border w-[75%] h-full m-auto">
    </div>
  </div>
</div>

<div class="bg-white w-full h-full py-7 min-h-[90vh]">
  <div class="w-full h-full py-7 min-h-screen flex items-center justify-center max-[500px]:flex-wrap">
    <div class="w-2/5 my-auto px-10 h-[65%] max-[500px]:w-full max-[500px]:h-[45%]">
      <img src="https://sadapmcmmm.blob.core.windows.net/strapi-uploads/assets/large_52853771003_50e48cbdb5_k_6f2e128095_8c59dea2e4.jpeg" alt="img" class="border w-[75%] max-w-[450px] h-full m-auto aspect-[12/8] rounded-md object-cover outline outline-2 outline-white lg:aspect-[10/12] lg:outline-8 max-[500px]:w-[90%]" style="object-position:79% 40%">
    </div>
    <div class="w-2/5 my-auto px-20 max-[500px]:w-full max-[500px]:px-10">
        <div class="text-5xl font-extrabold leading-tight uppercase max-[500px]:text-3xl" style="font-family: TuskerGrotesk, sans-serif;">Welcome to the Child Marriage Data Portal</div>
        <div class="text-lg tracking-wider my-3" style="font-family: Satoshi, sans-serif;">Child marriage robs girls of agency and bodily autonomy, often undermining their emotional, sexual and reproductive health. Data have the power to accelerate progress in ending this harmful practice by 2030, as called for in the Sustainable Development Goals. Read a brief overview of the Child Marriage Data Portal: its purpose, content and features.</div>
        <a href="/" class="text-lg tracking-wider my-3 underline underline-offset-4 text-blue-800 font-medium hover:no-underline" style="font-family: Satoshi, sans-serif;">Read this story</a>
        <a href="/" class="flex gap-3 text-nowrap items-center mt-10">
          <i class="fa fa-arrow-right flex items-center justify-center w-12 h-12 rounded-full text-red-500 border border-red-500 text-2xl"></i>
          <span class="text-lg font-medium">Go to stories</span>
        </a>
    </div>
  </div>
</div>



  
  <section id="focus" class="py-16 bg-gradient-to-b from-gray-200 to-f5e6c8">
    <div class="container mx-auto px-4 md:px-0$1">
      <h3 class="text-6xl font-bold font-anton mb-8 text-center">Core Areas of Focus</h3>
      <div class="grid md:grid-cols-3 gap-8">
        <div class="p-8 md:p-10 bg-white shadow-lg rounded-lg">
          <h4 class="text-3xl font-bold mb-4">Women Sexual Abuse</h4>
          <ul class="list-disc list-inside">
            <li>24x7 Support AI Chatbot: Legal, medical, rehabilitation support</li>
            <li>Support and advocacy for survivors</li>
            <li>Legal and emotional support</li>
            <li>Emergency connection to legal, medical, police services</li>
          </ul>
        </div>
        <div class="p-8 md:p-10 bg-white shadow-lg rounded-lg">
          <h4 class="text-3xl font-bold mb-4">Child Sexual Abuse</h4>
          <ul class="list-disc list-inside">
            <li>Protection and support for victims</li>
            <li>Collaboration with schools for safe environments</li>
            <li>AI chatbot for legal, medical, rehabilitation support</li>
            <li>Education programs for parents and children</li>
          </ul>
        </div>
        <div class="p-8 md:p-10 bg-white shadow-lg rounded-lg">
          <h4 class="text-3xl font-bold mb-4">Cyber Safety</h4>
          <ul class="list-disc list-inside">
            <li>Safe online practices</li>
            <li>Support for victims of online harassment</li>
            <li>Removal of offensive material</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
  
  <section id="programs" class="py-16 bg-gradient-to-b from-f5e6c8 to-white">
    <div class="container mx-auto px-4 md:px-0$1">
      <h3 class="text-6xl font-bold font-anton mb-8">Our Programs and Services</h3>
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div class="p-8 bg-white shadow rounded-lg">
          <h4 class="text-3xl font-bold mb-4">24/7 Helpline Services</h4>
          <p>Immediate support for survivors with medical, legal, and psychological needs.</p>
        </div>
        <div class="p-8 bg-white shadow rounded-lg">
          <h4 class="text-3xl font-bold mb-4">Counseling Services</h4>
          <p>Professional mental health support through counseling and peer groups.</p>
        </div>
        <div class="p-8 bg-white shadow rounded-lg">
          <h4 class="text-3xl font-bold mb-4">POSH Compliance Training</h4>
          <p>Training for workplaces and educational institutions to ensure safer environments.</p>
        </div>
        <div class="p-8 bg-white shadow rounded-lg">
          <h4 class="text-3xl font-bold mb-4">Vocational Training</h4>
          <p>Empowering survivors by providing skills for job placements and financial independence.</p>
        </div>
        <div class="p-8 bg-white shadow rounded-lg">
          <h4 class="text-3xl font-bold mb-4">Remarriage Support</h4>
          <p>Respectful re-entry into society by arranging remarriages for affected women.</p>
        </div>
        <div class="p-8 bg-white shadow rounded-lg">
          <h4 class="text-3xl font-bold mb-4">Legal Aid</h4>
          <p>Support for survivors in navigating the legal system and getting justice.</p>
        </div>
      </div>
    </div>
  </section>
  
  <section class="py-16 bg-gradient-to-b from-gray-800 to-black text-white">
    <div class="container mx-auto px-4 md:px-0.5 text-center">
      <h3 class="text-6xl font-bold font-anton mb-8">Join Our Fight</h3>
      <p class="text-lg max-w-2xl mx-auto mb-12">We are dedicated to ending sexual exploitation. Do you think it's high time to take action? Join us as a volunteer, partner, or donor to make a real impact today.</p>
      <a href="#contact" class="bg-white text-black px-8 py-4 rounded-lg text-lg font-bold">Get Involved</a>
    </div>
  </section>

<div class="footer w-full">
  <div class="bg-[#ced9d8] py-12 px-5 relative" style="background-image: url(grain.png);">
    <div class="bg-[#ced9d8] w-full h-full py-12 absolute top-0 left-0 bg-opacity-60"></div>
    <div class="max-w-[1496px] flex flex-wrap gap-2 justify-between m-auto mb-10 relative">
      <div class="w-[29%] min-w-60 max-[500px]:w-[80%] max-[500px]:m-auto max-[500px]:mb-6">
        <div class="max-w-[26ch] uppercase text-lg" style="font-family: Satoshi, sans-serif;">Data Centre & Resources</div>
        <div class="max-w-[26ch] uppercase text-[34px] font-bold" style="font-family: TuskerGrotesk, sans-serif;">Download the data</div>
        <div class="font-medium" style="font-family: Satoshi, sans-serif;">Download datasets featuring global, regional and national data and explore resources, including the latest publications, articles and tools relevant to child marriage monitoring.</div>
        <a href="/" class="flex gap-3 text-nowrap items-center mt-8">
          <i class="fa fa-arrow-right flex items-center justify-center w-12 h-12 rounded-full text-red-500 border border-red-500 text-2xl"></i>
          <span class="text-lg font-medium">Go to Data Center</span>
        </a>
      </div>
      <div class="w-[29%] min-w-60 max-[500px]:w-[80%] max-[500px]:m-auto max-[500px]:mb-6">
        <div class="max-w-[26ch] uppercase text-lg" style="font-family: Satoshi, sans-serif;">About Us</div>
        <div class="max-w-[26ch] uppercase text-[34px] font-bold" style="font-family: TuskerGrotesk, sans-serif;">The Mechanism</div>
        <div class="font-medium" style="font-family: Satoshi, sans-serif;">The Child Marriage Monitoring Mechanism relies on the power of data to accelerate progress in ending child marriage by 2030, as called for in the Sustainable Development Goals.</div>
        <a href="/" class="flex gap-3 text-nowrap items-center mt-8">
          <i class="fa fa-arrow-right flex items-center justify-center w-12 h-12 rounded-full text-red-500 border border-red-500 text-2xl"></i>
          <span class="text-lg font-medium">More About Us</span>
        </a>
      </div>
      <div class="w-[29%] min-w-60 max-[500px]:w-[80%] max-[500px]:m-auto">
        <div class="max-w-[26ch] uppercase text-lg" style="font-family: Satoshi, sans-serif;">Subscribe</div>
        <div class="max-w-[26ch] uppercase text-[34px] font-bold" style="font-family: TuskerGrotesk, sans-serif;">Newsletter</div>
        <div class="font-medium mb-5" style="font-family: Satoshi, sans-serif;">Enter your email to stay up to date on the latest child marriage data.</div>
        <input type="text" class="border rounded-md px-5 py-2.5 bg-white outline-none focus:border-2 w-[90%]" placeholder="Enter your email">
        <a href="/" class="flex gap-3 text-nowrap items-center mt-8">
          <i class="fa fa-arrow-right flex items-center justify-center w-12 h-12 rounded-full text-red-500 border border-red-500 text-2xl"></i>
          <span class="text-lg font-medium">Subscribe</span>
        </a>
      </div>
    </div>
  </div>
  <div class="bg-[#ff806d] py-12 px-5 relative" style="background-image: url(grain.png);">
    <div class="bg-[#ff806d] w-full h-full py-12 absolute top-0 left-0 bg-opacity-65"></div>
    <div class="container mx-auto py-12 relative">
      <div class="flex justify-between text-xl font-medium flex-wrap max-[500px]:block max-[500px]:space-y-5 max-[500px]:p-4">
          <div>
              <h1 class="text-black font-bold text-3xl">THE CHILD<br>MARRIAGE<br>DATA PORTAL</h1>
          </div>
          <div>
              <ul class="text-black space-y-4">
                <li>Home</li>
                <li>Global Trends & SDG Progress</li>
                <li>Country Profiles</li>
                <li>Data Centre & Resources</li>
              </ul>
          </div>
          <div>
            <ul class="text-black space-y-4">
              <li>Stories</li>
              <li>About Us</li>
              <li>FAQs</li>
              <li>Contact</li>
            </ul>
          </div>
          <div class="">
            <p class="text-black mt-12">X (formerly known as Twitter)</p>
            <p class="text-black mt-6">Write us:<br>childmarriagemonitoring@unicef.org</p>
          </div>
      </div>
    </div>
  </div>
  <footer class="bg-black bg-opacity-70 py-12 px-5 text-white" style="background-image: url(Rectangle.png);background-blend-mode: multiply;">
      <div class="container mx-auto">
          <p class="text-sm">
              This initiative is generously supported by the governments of Belgium, Canada, Italy, the Netherlands, Norway, the United Kingdom and the United States, the European Union and Zonta International.
          </p>
          <p class="text-sm mt-4">
              Except where otherwise noted, content on this site is licensed under a Creative Commons Attribution-NonCommercial 3.0 IGO license.
          </p>
          <p class="text-sm mt-4">
              Photos courtesy of UNICEF.
          </p>
          <div class="mt-8 text-sm flex justify-between items-center">
              <span>Legal Info</span>
              <span>UNICEF, 2024.</span>
          </div>
      </div>
  </footer>
</div>


