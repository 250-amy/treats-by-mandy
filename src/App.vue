<script setup>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

const weddings = [
  { id: '1', url: '/wedding.jpg' },
  { id: '2', url: '/wedding-2.jpg' },
  { id: '3', url: '/wedding-3.jpg' },
  { id: '4', url: '/wedding-4.jpg' },
  { id: '5', url: '/wedding-5.jpg' },
]

const birthdays = [
  { id: '1', url: '/birthday.jpg' },
  { id: '2', url: '/birthday-2.jpg' },
  { id: '3', url: '/birthday-3.jpg' },
  { id: '4', url: '/birthday-4.jpg' },
  { id: '5', url: '/birthday-5.jpg' },
]

const kids = [
  { id: '1', url: '/kids.jpg' },
  { id: '2', url: '/kids-2.jpg' },
  { id: '3', url: '/kids-3.jpg' },
  { id: '4', url: '/kids-4.jpg' },
  { id: '5', url: '/kids-5.jpg' },
]

</script>


<template>
<div class="main">
  

<!-- Beginning of hero section -->
  <div class="w-screen lg:h-screen flex flex-col items-center md:flex-row justify-center space-x-10 lg:space-x-48 bg-gradient-to-tl from-[#97B1B1] via-[#C6D4D4] to-[#E0E8E8]">
    <div class='bg-[url("/gold-dots.png")] w-auto bg-left-top flex bg-no-repeat'>
    <div class="max-w-[500px] lg:my-auto flex items-center">
      <div class="ml-[50px] lg:ml-[20px] mt-16 mr-[80px]">
        <div class="max-w-[250px] lg:max-w-[450px]">
          <h1 class="lg:text-[13em] lg:leading-[10rem]">Treats</h1>
          <h2 class="mb-8 lg:text-[2em]">By Mandy</h2>
        </div>
        <p class="mb-8">Ottawa-based baker creating personalized cakes, cupcakes, and treats for any occasion.</p>

        <div class="socials flex flex-col items-center">
          <a href="#contact"><button class="my-4 px-8 py-1 text-lg lg:text-xl uppercase bg-white hover:bg-[#597373] hover:text-white ease-in-out duration-300 text-gray-700 font-medium tracking-wider border-2 border-[#597373] rounded-3xl shadow">Order Now!</button></a>
          <ul class="flex space-x-3">
            <li>
              <a href="https://www.facebook.com/treatsbymandy" type="button" class="rounded-full border-2 border-[#597373] text-[#597373] leading-normal uppercase hover:bg-white hover:bg-opacity-25 focus:outline-none focus:ring-0 transition duration-150 ease-in-out w-9 h-9 m-1 flex justify-center items-center">
                <v-icon name="fa-facebook-f" />
            </a>
            </li>
            <li>
              <a href="https://www.instagram.com/treats.by.mandy/" type="button" class="rounded-full border-2 border-[#597373] text-[#597373] leading-normal uppercase hover:bg-white hover:bg-opacity-25 focus:outline-none focus:ring-0 transition duration-150 ease-in-out w-9 h-9 m-1 flex justify-center items-center">
                <v-icon name="bi-instagram" />
            </a>
            </li>
          <li>
            <a href="#!" type="button" class="rounded-full border-2 border-[#597373] text-[#597373] leading-normal uppercase hover:bg-white hover:bg-opacity-25 focus:outline-none focus:ring-0 transition duration-150 ease-in-out w-9 h-9 m-1 flex justify-center items-center">
              <v-icon name="bi-google" />
            </a>
          </li>
          </ul>
        </div>
      </div>
    </div>
  </div>


    <div class="mt-auto max-w-[400px] md:max-w-[600px] mr-[176px]"> 
      <div class="p-10 bg-white mr-[10px]">
        <div class="ml-[-70px] md:ml-[-100px] bg-[conic-gradient(at_top_left,_var(--tw-gradient-stops))] from-orange-900 via-amber-100 to-orange-900">
          <img src="/main.jpg" alt="main section wedding cake image" class="drop-shadow-[0_25px_25px_rgba(0,0,0,0.25)] p-1 md:max-h-[600px]">
        </div>
      </div>
    </div>


</div>

<!-- Beginning of wedding section -->
  <div class="wedding flex flex-col items-center md:flex-row justify-center max-h-[500px] md:max-h-[400px] my-32 md:my-56 space-x-8 lg:space-x-32 bg-gradient-to-r from-[#EBC8D0] via-[#ECD5D5] to-[#EDD8D8] w-screen">
    <div class="md:ml-16 md:pl-8 max-w-[270px] md:max-w-[500px]"> 
      <div class="p-10 bg-white shadow-lg">
        <div class="max-w-[300px] md:max-w-[400px]">
<carousel :items-to-show="1">
    <Slide v-for="slide in weddings" :key="slide.id">
      <div class="max-w-[300px] md:max-w-[400px] w-96">
        <div class="bg-[conic-gradient(at_top_left,_var(--tw-gradient-stops))] from-orange-900 via-amber-100 to-orange-900">
          <img :src="slide.url" alt="wedding cake" class="p-1"/>
        </div>
      </div>
    </slide>

    <template #addons>
      <navigation />
      <pagination />
    </template>
  </carousel>
  </div>
      </div>
    </div>

    <div class="flex items-center w-full justify-center md:pr-16">
      <div class="flex flex-col max-w-md mr-8 lg:mr-0">
        <h3 class="text-2xl md:text-4xl mb-2 mt-3 md:mt-0 text-center md:text-start">Weddings</h3>
        <span class="text-[#66444C] text-sm md:text-lg lg:text-xl pb-8 md:pb-0">Information about wedding cakes goes here. Information about wedding cakes goes here. Information about wedding cakes goes here.  Information about wedding cakes goes here. Information about wedding cakes goes here.</span>
      </div>
    </div>

  </div>

<!-- Beginning of birthdays section -->

<div class="birthdays flex flex-col items-center md:flex-row justify-center max-h-[500px] md:max-h-[400px] my-32 md:my-56 md:space-x-8 lg:space-x-32 bg-gradient-to-l from-[#BCD2C6] via-[#CCDCD3] to-[#E1EBE5] w-screen">

  <div class="flex items-center w-full justify-center md:pl-16 pt-8 md:pt-0">
      <div class="flex flex-col max-w-md mx-4 lg:ml-0">
        <h3 class="text-2xl md:text-4xl mb-2 text-center md:text-start">Birthdays</h3>
        <span class="text-[#405248] text-sm md:text-lg lg:text-xl pb-3 md:pb-0">Information about birthday cakes goes here. Information about birthday cakes goes here. Information about birthday cakes goes here. Information about birthday cakes goes here. Information about birthday cakes goes here. </span>
      </div>
    </div>

  <div class="md:pr-8 md:mr-16 max-w-[270px] md:max-w-[500px]"> 
      <div class="p-10 bg-white shadow-lg">
        <div class="max-w-[300px] md:max-w-[400px]">
<carousel :items-to-show="1">
    <Slide v-for="slide in birthdays" :key="slide.id">
      <div class="max-w-[300px] md:max-w-[400px] w-96">
        <div class="bg-[conic-gradient(at_top_left,_var(--tw-gradient-stops))] from-orange-900 via-amber-100 to-orange-900">
          <img :src="slide.url" alt="birthday cake" class="p-1"/>
        </div>
      </div>
    </slide>

    <template #addons>
      <navigation />
      <pagination />
    </template>
  </carousel>
  </div>
      </div>
    </div>

</div>

<!-- Beginning of kids section -->
<div class="kids flex flex-col items-center md:flex-row justify-center max-h-[500px] md:max-h-[400px] md:my-48 space-x-8 lg:space-x-32 bg-gradient-to-r from-[#97B1B1] via-[#A5BBBB] to-[#B4C7C7] w-screen">
    <div class="md:ml-16 md:pl-8 max-w-[270px] md:max-w-[500px]"> 
      <div class="p-10 bg-white shadow-lg">
        <div class="max-w-[300px] md:max-w-[400px]">
<carousel :items-to-show="1">
    <Slide v-for="slide in kids" :key="slide.id">
      <div class="max-w-[300px] md:max-w-[400px] w-96">
        <div class="bg-[conic-gradient(at_top_left,_var(--tw-gradient-stops))] from-orange-900 via-amber-100 to-orange-900">
          <img :src="slide.url" alt="kids party cake" class="p-1"/>
        </div>
      </div>
    </slide>

    <template #addons>
      <navigation />
      <pagination />
    </template>
  </carousel>
  </div>
      </div>
    </div>

    <div class="flex items-center w-full justify-center md:pr-16">
      <div class="flex flex-col max-w-md mr-8 lg:mr-0">
        <h3 class="text-2xl md:text-4xl mb-2 mt-3 md:mt-0 text-center md:text-start">Kids'&nbsp;Parties</h3>
        <span class="text-[#2C3737] text-sm md:text-lg lg:text-xl pb-8 md:pb-0">Information about kid's cakes goes here. Information about kid's cakes goes here. Information about kid's cakes goes here. Information about kid's cakes goes here. Information about kid's cakes goes here.</span>
      </div>
    </div>

  </div>

<!-- Beginning of more section -->
<div class="more flex flex-col md:flex-row justify-center items-center space-y-8 lg:space-x-20 w-screen my-8 md:my-32 px-8 md:px-12 lg:px-20">
  <div class="w-72 md:w-72 text-center">
    <h4 class="text-xl md:text-2xl lg:text-3xl">AND MORE</h4>
    <p class="text-sm md:text-lg">Text here</p>
  </div>
  <div class="w-72 md:w-72 text-center">
    <h4 class="text-xl md:text-2xl lg:text-3xl">AND MORE</h4>
    <p class="text-sm md:text-lg">If you have other types of cakes and desserts that you would like to highlight, we can put those in this section. </p>
  </div>
  <div class="w-72 md:w-72 text-center">
    <h4 class="text-xl md:text-2xl lg:text-3xl">AND MORE</h4>
    <p class="text-sm md:text-lg">Text here</p>
  </div>
</div>

<!-- Beginning of testimonials section -->
<div class="more bg-gradient-to-l from-[#CBBB81] via-[#D6C99B] to-[#DFD5B2] w-screen">
  <div class="flex justify-center items-center">
    <div class="flex flex-col items-start md:my-10 p-8 md:p-10">
    <h3 class="text-2xl md:text-4xl mb-6">What people are saying</h3>
    <div class="flex flex-col md:flex-row justify-center md:space-x-6 lg:space-x-8">
      <div class="bg-white rounded-xl shadow-lg p-6 w-80 md:w-60 lg:w-80 mb-4 md:mb-0">
        <h4 class="mb-2 font-bold md:text-xl">
          <p>“flawless experience”</p>
        </h4>
        <div class="mb-4 flex flex-wrap">
            <img src="/star.png">
            <img src="/star.png">
            <img src="/star.png">
            <img src="/star.png">
            <img src="/star.png">
        </div>
        <p class="text-sm md:text-[16px]">I had such a wonderful and flawless experience with Mandy. Excellent communication and extremely talented! The wedding cake was gorgeous and delicious!</p>
        <p class="text-sm md:text-[16px] text-right mr-8">— Pri M</p>
      </div>

      <div class="bg-white rounded-xl shadow-lg p-6 w-80 md:w-60 lg:w-80 mb-4 md:mb-0">
        <h4 class="mb-2 font-bold md:text-xl">
          <p>“Highly recommend”</p>
        </h4>
        <div class="mb-4 flex flex-wrap">
            <img src="/star.png">
            <img src="/star.png">
            <img src="/star.png">
            <img src="/star.png">
            <img src="/star.png">
        </div>
        <p class="text-sm md:text-[16px]">Treats by Mandy has become a staple in our house for celebrations, specially birthdays.  Cupcakes or cake, chocolate or vanilla, we're always impressed with the creativity she puts into her cakes without sacrificing flavour! </p>
        <p class="text-sm md:text-[16px] text-right mr-8">— Eric M</p>
      </div>

      <div class="bg-white rounded-xl shadow-lg p-6 w-80 md:w-60 lg:w-80">
        <h4 class="mb-2 font-bold md:text-xl">
          <p>“absolutely delicious”</p>
        </h4>
        <div class="mb-4 flex flex-wrap">
            <img src="/star.png">
            <img src="/star.png">
            <img src="/star.png">
            <img src="/star.png">
            <img src="/star.png">
        </div>
        <p class="text-sm md:text-[16px]">Mandy’s imagination and creativity bring your cake and dessert dreams to life. She works with you to ensure your order is exactly as you envisioned- extravagant, simple, elegant, or wacky!</p>
        <p class="text-sm md:text-[16px] text-right mr-8">— Agata A</p>
      </div>
    </div>
  </div>
  </div>
</div>

<!-- Beginning of instagram section -->
<div class="instagram flex flex-col md:flex-row items-center justify-center bg-white w-screen my-20 px-48 md:space-x-20">
  <div class="logo mb-10 md:mb-0">
    <img src="/logo.png" class="max-w-[300px]">
  </div>
  <div class="w-72 md:w-72 text-center">
    <p class="text-sm md:text-lg">This is where we could embed your instagram feed</p>
  </div>
</div>

<!-- Beginning of contact section -->
<div class="contact bg-gradient-to-bl from-[#97B1B1] via-[#C6D4D4] to-[#E0E8E8]  w-screen">
<div class="flex justify-center">
  <div class="container flex justify-center">
    <div class="max-w-4xl my-8 px-10">
      <div class="">
        <h3 id="contact" class="text-2xl md:text-4xl mb-6">Let's get in touch</h3>
        <p class="mb-10">Have questions? Want to place an order? Message me on Facebook or Instagram, or complete the following form. I will get back to you ASAP!</p>
        <form action="https://api.web3forms.com/submit" method="POST" id="form">
          <input type="hidden" name="access_key" value="bc628b01-4ec9-424d-a49f-2c587c215f74" />
          <input type="hidden" name="subject" value="New Submission from Web3Forms" />
          <input type="hidden" name="redirect" value="https://web3forms.com/success" />
          <input type="checkbox" name="botcheck" id="" style="display: none;" />
          <div class="mb-6">
            <label for="name" class="block mb-2 text-sm text-gray-600 uppercase">Full Name</label>
            <input type="text" name="name" id="name" placeholder="John Doe" required class="w-full px-3 py-2 placeholder-gray-500 border italic border-gray-300 rounded-md focus:outline-none focus:ring focus:ring-white focus:border-cyan-700 bg-white" />
          </div>
          <div class="flex flex-col md:flex-row justify-between">
          <div class="mb-6 flex flex-col w-full">
            <label for="email" class="mb-2 text-sm text-gray-600 uppercase">Email Address</label>
            <input type="email" name="email" id="email" placeholder="you@company.com" required class="w-full px-3 py-2 placeholder-gray-500 italic border border-gray-300 rounded-md focus:outline-none focus:ring focus:ring-white focus:border-cyan-700 bg-white" />
          </div>
          <div class="mb-6 flex flex-col w-full">
            <label for="phone" class="mb-2 text-sm text-gray-600 uppercase">Phone Number (not required)</label>
            <input type="text" name="phone" id="phone" placeholder="+1 (555) 123-4567" class="w-full px-3 py-2 placeholder-gray-500 border italic border-gray-300 rounded-md focus:outline-none focus:ring focus:ring-white focus:border-cyan-700 bg-white" />
          </div>
          </div>
          <div class="mb-6">
            <label for="message" class="block mb-2 text-sm text-gray-600 uppercase">Your Message</label>

            <textarea rows="5" name="message" id="message" placeholder="Message" class="w-full px-3 py-2 placeholder-gray-500 border italic border-gray-300 rounded-md focus:outline-none focus:ring focus:ring-white focus:border-cyan-700 bg-white" required></textarea>
          </div>
          <div class="mb-6">
            <button type="submit" class="w-full px-3 py-4 text-white uppercase tracking-wider font-semibold bg-[#9AB3B3] rounded-md hover:bg-[#7D9696] focus:outline-none ease-in-out duration-300">
              Send Message
            </button>
          </div>
          <p class="text-base text-center text-gray-400" id="result"></p>
        </form>
      </div>
    </div>
  </div>
</div>

</div>

<!-- Footer -->
<footer class="w-screen flex flex-col items-center justify-between py-2 px-6 bg-white sm:flex-row">
    <p class="text-sm md:text-md font-medium">Treats by Mandy</p>

    <p class="text-sm text-gray-600">© Copyright 2021. All Rights Reserved.</p>

    <div class="flex">
        <a href="https://www.instagram.com/treats.by.mandy/" class="mr-6 text-gray-600 hover:text-gray-400">
        <svg
          aria-hidden="true"
          focusable="false"
          data-prefix="fab"
          data-icon="instagram"
          class="svg-inline--fa fa-instagram w-5"
          role="img"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 448 512"
        >
          <path
            fill="currentColor"
            d="M224.1 141c-63.6 0-114.9 51.3-114.9 114.9s51.3 114.9 114.9 114.9S339 319.5 339 255.9 287.7 141 224.1 141zm0 189.6c-41.1 0-74.7-33.5-74.7-74.7s33.5-74.7 74.7-74.7 74.7 33.5 74.7 74.7-33.6 74.7-74.7 74.7zm146.4-194.3c0 14.9-12 26.8-26.8 26.8-14.9 0-26.8-12-26.8-26.8s12-26.8 26.8-26.8 26.8 12 26.8 26.8zm76.1 27.2c-1.7-35.9-9.9-67.7-36.2-93.9-26.2-26.2-58-34.4-93.9-36.2-37-2.1-147.9-2.1-184.9 0-35.8 1.7-67.6 9.9-93.9 36.1s-34.4 58-36.2 93.9c-2.1 37-2.1 147.9 0 184.9 1.7 35.9 9.9 67.7 36.2 93.9s58 34.4 93.9 36.2c37 2.1 147.9 2.1 184.9 0 35.9-1.7 67.7-9.9 93.9-36.2 26.2-26.2 34.4-58 36.2-93.9 2.1-37 2.1-147.8 0-184.8zM398.8 388c-7.8 19.6-22.9 34.7-42.6 42.6-29.5 11.7-99.5 9-132.1 9s-102.7 2.6-132.1-9c-19.6-7.8-34.7-22.9-42.6-42.6-11.7-29.5-9-99.5-9-132.1s-2.6-102.7 9-132.1c7.8-19.6 22.9-34.7 42.6-42.6 29.5-11.7 99.5-9 132.1-9s102.7-2.6 132.1 9c19.6 7.8 34.7 22.9 42.6 42.6 11.7 29.5 9 99.5 9 132.1s2.7 102.7-9 132.1z"
          ></path>
        </svg>
      </a>

      <a href="https://www.facebook.com/treatsbymandy" class="text-gray-600 hover:text-gray-400">
      <svg
        aria-hidden="true"
        focusable="false"
        data-prefix="fab"
        data-icon="facebook-f"
        class="svg-inline--fa fa-facebook-f w-3"
        role="img"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 320 512"
      >
        <path
          fill="currentColor"
          d="M279.14 288l14.22-92.66h-88.91v-60.13c0-25.35 12.42-50.06 52.24-50.06h40.42V6.26S260.43 0 225.36 0c-73.22 0-121.08 44.38-121.08 124.72v70.62H22.89V288h81.39v224h100.17V288z"
        ></path>
      </svg>
      </a>

    </div>
</footer>

</div>
  
</template>


