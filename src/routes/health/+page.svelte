<script>
    let options = false;
    let imgArr = [
      "https://platinumlist.net/guide/wp-content/uploads/2023/03/IMG-worlds-of-adventure.webp",
      "https://dynamic-media-cdn.tripadvisor.com/media/photo-o/0f/ba/29/5c/img-worlds-of-adventure.jpg?w=900&h=500&s=1",
      "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcREHjj0QVmfJLo5BrdEKQZ5td36QsOqjgTQFg&s"
    ];
    let currentImage = 0;
    let direction = 1; // 1 for next, -1 for previous

    function prev() {
        direction = -1;
        currentImage = (currentImage === 0) ? imgArr.length - 1 : currentImage - 1;
    }

    function next() {
        direction = 1;
        currentImage = (currentImage + 1) % imgArr.length;
    }
</script>
<div class="main w-full text-gray-800 max-w-[1400px] m-auto">
    <div class="Header fixed top-0 w-full max-w-[1400px] bg-white bg-opacity-80 backdrop-blur px-5 z-50">
        <div class="flex items-center justify-between w-full py-2 border-b">
            <img src="VITAFORM.png" alt="Logo" class="w-32 max-[1080px]:w-28">
            <div class="flex items-center gap-5 font-medium max-[640px]:hidden">
                <a href="/" class="p-2 text-gray-600 hover:text-black">Home</a>
                <a href="/" class="p-2 text-gray-600 hover:text-black">Exercise</a>
                <a href="/" class="p-2 text-gray-600 hover:text-black">Features</a>
                <a href="/" class="p-2 text-gray-600 hover:text-black">Services</a>
                <a href="/" class="p-2 text-gray-600 hover:text-black">Premium</a>
            </div>
            <div class="sm:hidden px-2 py-1.5">
                <i class="fa fa-bars" on:click={() => {options = !options}}></i>
                {#if options}
                    <div class="w-44 absolute top-14 right-4 grid p-1 space-y-1 bg-white bg-opacity-80 backdrop-blur rounded-md border z-50">
                      <a href="/" class="px-3 py-1">Home</a>
                      <a href="/" class="px-3 py-1">Exercise</a>
                      <a href="/" class="px-3 py-1">Features</a>
                      <a href="/" class="px-3 py-1">Services</a>
                      <a href="/" class="px-3 py-1">Premium</a>
                    </div>
                {/if}
            </div>
        </div>
    </div>
    <div class="w-full h-screen max-h-[700px] p-2 relative">
        <div class="absolute bottom-6 left-0 px-8">
            <div class="space-y-4">
                <div class="">Strong is the simplest, most intuitive workout tracking experience.<br>Trusted by over 3 million users worldwide.</div>
                <div class="w-fit bg-red-600 text-red-600 px-1.5 py-1 cursor-pointer" style="clip-path: polygon(15% 0, 85% 0, 100% 50%, 85% 100%, 15% 100%, 0% 50%);">
                    <div class="bg-white text-red-600 py-1 px-5 hover:bg-red-600 hover:text-white" style="clip-path: polygon(13% 0, 87% 0, 100% 50%, 87% 100%, 13% 100%, 0% 50%);">Schedule a Call</div>
                </div>
            </div>
            <div class="flex items-center gap-2 mt-16">
                <div class="grid">
                    <span class="text-lg font-medium">3.2k</span>
                    <span class="text-xs">Happy User</span>
                </div>
                <div class="grid">
                    <span class="text-lg font-medium">350k</span>
                    <span class="text-xs">Running Track</span>
                </div>
                <div class="grid">
                    <span class="text-lg font-medium">100+</span>
                    <span class="text-xs">Workout Type</span>
                </div>
            </div>
        </div>
    </div>
    <div class="w-full p-2">
        <div class="flex items-center justify-evenly p-5 max-sm:flex-col max-sm:space-y-7">
            <div class="max-w-[22%] min-w-48">
                <div class="space-y-1">
                    <div class="flex items-center gap-2">
                        <div class="flex -space-x-3">
                            <div class="rounded-full border w-6 h-6"></div>
                            <div class="rounded-full border w-6 h-6"></div>
                            <div class="rounded-full border w-6 h-6"></div>
                        </div>
                        <div class="text-2xl font-medium">120K+</div>
                    </div>
                    <div class="text-gray-800 text-sm max-sm:break-all">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aliquid, vitae!</div>
                </div>
            </div>
            <div class="max-w-[22%] min-w-48">
                <div class="space-y-1">
                    <div class="flex items-center gap-2">
                        <i class="fa fa-star text-yellow-300"></i>
                        <div class="text-2xl font-medium">4.8</div>
                    </div>
                    <div class="text-gray-800 text-sm max-sm:break-all">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aliquid, vitae!</div>
                </div>
            </div>
            <div class="max-w-[22%] min-w-48">
                <div class="space-y-1">
                    <div class="flex items-center">
                        <div class="text-2xl font-medium">100+</div>
                    </div>
                    <div class="text-gray-800 text-sm max-sm:break-all">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aliquid, vitae!</div>
                </div>
            </div>
        </div>
    </div>
    <div class="w-full p-2 mt-12">
        <div class="flex w-full h-[90vh] max-h-[600px] max-[580px]:block max-[580px]:h-full max-[580px]:max-h-full max-[580px]:space-y-5">
            <div class="w-1/3 pl-8 pr-2 relative max-[800px]:w-[45%] max-[580px]:w-full">
                <div class="text-4xl font-medium">Move to Maintain your Health</div>
                <div class="text-base mb-4">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Error commodi necessitatibus quaerat provident est omnis iusto facilis sint voluptatum voluptas in, sunt qui numquam temporibus deleniti molestiae odit excepturi expedita.</div>
                <div class="w-fit bg-red-600 text-red-600 px-1.5 py-1 cursor-pointer" style="clip-path: polygon(15% 0, 85% 0, 100% 50%, 85% 100%, 15% 100%, 0% 50%);">
                    <div class="bg-white text-red-600 py-1 px-5 text-sm hover:bg-red-600 hover:text-white" style="clip-path: polygon(13% 0, 87% 0, 100% 50%, 87% 100%, 13% 100%, 0% 50%);">Schedule a Call</div>
                </div>
                <div class="flex items-center gap-5 mt-10 w-fit m-auto absolute bottom-8 right-4 max-[580px]:bottom-1">
                    <div class="flex items-center justify-center rounded-full w-8 h-8 bg-white hover:bg-slate-100 shadow cursor-pointer" on:click={prev}>
                        <i class="fa fa-angle-left"></i>
                    </div>
                    <div class="flex items-center justify-center rounded-full w-8 h-8 bg-white hover:bg-slate-100 shadow cursor-pointer" on:click={next}>
                        <i class="fa fa-angle-right"></i>
                    </div>
                </div>
            </div>
            <div class="w-2/3 h-full flex items-center justify-center max-[800px]:w-[55%] max-[580px]:w-full">
                <img src="{imgArr[currentImage]}" alt="img" class="transition-opacity duration-500 w-[90%] h-[90%]">
            </div>
        </div>
    </div>
    <div class="w-full p-2 mt-12">
        <div class="w-full">
            <h1 class="text-4xl text-center font-medium w-1/3 min-w-[340px] m-auto max-w-96 max-[460px]:text-2xl max-[460px]:max-w-80 max-[380px]:min-w-24 max-[380px]:w-full">Achieve your Health Objectives in 1-2-3</h1>
            <div class="grid grid-cols-2 grid-rows-2 max-[640px]:block max-[640px]:space-y-9 max-[640px]:py-9">
                <div class="flex items-center justify-end h-60 max-[640px]:justify-center max-[640px]:h-auto">
                    <div class="card w-72 space-y-3 max-[460px]:w-64">
                        <div class="rounded-full w-10 h-10 bg-red-800"></div>
                        <h2 class="text-xl font-medium pb-3">Smarter Traning</h2>
                        <span class="text-sm text-gray-700">Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit, architecto.sit amet consectetur adipisicing elit</span>
                    </div>
                </div>
                <div class="row-span-2 flex items-center justify-start h-60 my-auto max-[640px]:justify-center max-[640px]:h-auto">
                    <div class="card w-72 space-y-3 max-[460px]:w-64">
                        <div class="rounded-full w-10 h-10 bg-red-800"></div>
                        <h2 class="text-xl font-medium pb-3">Strong Community</h2>
                        <span class="text-sm text-gray-700">Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit, architecto.sit amet consectetur adipisicing elit</span>
                    </div>
                </div>
                <!-- <div class="row-span-2 flex items-center justify-start max-[640px]:justify-center max-[640px]:h-auto">
                    <div class="card w-72 space-y-3 p-5 max-[640px]:p-0 max-[460px]:w-64">
                        <div class="rounded-full w-10 h-10 bg-red-800"></div>
                        <h2 class="text-xl font-medium pb-3">Strong Community</h2>
                        <span class="text-sm text-gray-700">Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit, architecto.sit amet consectetur adipisicing elit</span>
                        <div class="h-12 border"></div>
                        <div class="h-12 border"></div>
                    </div>
                </div> -->
                <div class="flex items-center justify-end h-60 max-[640px]:justify-center max-[640px]:h-auto">
                    <div class="card w-72 space-y-3 max-[460px]:w-64">
                        <div class="rounded-full w-10 h-10 bg-red-800"></div>
                        <h2 class="text-xl font-medium pb-3">Custom Workouts</h2>
                        <span class="text-sm text-gray-700">Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit, architecto.sit amet consectetur adipisicing elit</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="w-full p-2 mt-12">
        <div class="w-full flex">
            <div class="w-2/5 max-[760px]:w-1/5 max-[600px]:w-0"></div>
            <div class="w-3/5 px-8 max-[760px]:w-4/5 max-[600px]:w-full">
                <div class="text-xs">Achieve your Goals</div>
                <h1 class="font-medium text-3xl max-[450px]:text-2xl">Personalized Insights and Recommendations</h1>
                <div class="flex justify-between mt-4">
                    <div class="flex items-center gap-2">
                        <div class="flex items-center justify-center rounded-full w-8 h-8 bg-white hover:bg-slate-50 shadow cursor-pointer" on:click={prev}>
                            <i class="fa fa-angle-left"></i>
                        </div>
                        <div class="flex items-center justify-center rounded-full w-8 h-8 bg-white hover:bg-slate-50 shadow cursor-pointer" on:click={next}>
                            <i class="fa fa-angle-right"></i>
                        </div>
                    </div>
                    <div class="text-sm w-1/2 max-[760px]:w-2/3 max-[450px]:line-clamp-5">Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum nesciunt, velit quaerat distinctio voluptates modi facilis dolore illo sed sint nobis libero mollitia fugit! Ratione nisi earum dignissimos id non.</div>
                </div>
            </div>
        </div>
        <div class="carousal w-full h-96 mt-8 px-4 max-[600px]:h-60">
            <div class="flex items-center gap-4 h-full">
                <div class="box border h-full w-1/3 rounded-md max-[550px]:w-1/2">
                    <img src="https://platinumlist.net/guide/wp-content/uploads/2023/03/IMG-worlds-of-adventure.webp" alt="img" class="w-full h-full">
                </div>
                <div class="box border h-full w-1/3 rounded-md max-[550px]:w-1/2">
                    <img src="https://platinumlist.net/guide/wp-content/uploads/2023/03/IMG-worlds-of-adventure.webp" alt="img" class="w-full h-full">
                </div>
                <div class="box border h-full w-1/3 rounded-md max-[550px]:hidden">
                    <img src="https://platinumlist.net/guide/wp-content/uploads/2023/03/IMG-worlds-of-adventure.webp" alt="img" class="w-full h-full">
                </div>
            </div>
        </div>
    </div>
    <div class="w-full p-8 mt-12">
        <div class="flex items-center gap-2 max-[760px]:flex-col">
            <div class="bg-yellow-300 p-8 w-[30%] min-w-80 h-[400px] rounded-xl overflow-hidden max-[760px]:w-full max-[400px]:min-w-64">
                <h2 class="text-2xl font-medium text-center mb-6">Track your Health Progress</h2>
                <div class="flex items-center justify-between gap-2 w-[90%] m-auto max-[1100px]:text-sm max-[400px]:grid">
                  <button class="bg-black text-white cursor-pointer px-3 py-2 rounded-md">Google Play</button>
                  <button class="bg-black text-white cursor-pointer px-3 py-2 rounded-md">App Store</button>
                </div>
                <img src="/" alt="img" class="w-full h-auto">
            </div>
            <div class="bg-blue-300 w-[70%] h-[400px] rounded-xl overflow-hidden max-[760px]:w-full">
                <img src="DailySteps.png" alt="img" class="w-full h-full">
            </div>
        </div>
    </div>
    <div class="w-full p-2 mt-12">
        <div class="w-full">
            <h1 class="text-4xl text-center font-medium w-1/3 min-w-[340px] m-auto max-w-96 max-[460px]:text-2xl max-[460px]:max-w-80 max-[380px]:min-w-24 max-[380px]:w-full">Getting Started is Simple Use!</h1>
            <div class="w-[70%] m-auto flex items-center my-10 max-[650px]:block">
                <div class="w-1/2 max-[650px]:w-full">
                    <img src="" alt="img" class="w-[90%] m-auto h-auto">
                    <div class="">
                        <h2 class="text-3xl font-semibold">Download the App</h2>
                        <span class="text-xs">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Veritatis, saepe.</span>
                    </div>
                </div>
                <div class="w-1/2 max-[650px]:w-full">
                    <img src="" alt="img" class="w-[90%] m-auto h-auto">
                    <div class="">
                        <h2 class="text-3xl font-semibold">Create & Personalized</h2>
                        <span class="text-xs">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Veritatis, saepe.</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <footer class="bg-gray-100 text-gray-700 py-10 font-sans">
        <div class="container mx-auto px-6">
            <div class="flex justify-around items-center mb-12 max-[880px]:block">
                <div class="space-y-3">
                    <img src="VITAFORM.png" alt="img" class="w-48">
                    <div class="flex space-x-2">
                        <button class="border border-gray-300 rounded-full p-1 transition-colors hover:bg-gray-200 flex items-center justify-center w-8 h-8" ><i class="fa fa-facebook"></i></button>
                        <button class="border border-gray-300 rounded-full p-1 transition-colors hover:bg-gray-200 flex items-center justify-center w-8 h-8" ><i class="fa fa-twitter"></i></button>
                        <button class="border border-gray-300 rounded-full p-1 transition-colors hover:bg-gray-200 flex items-center justify-center w-8 h-8" ><i class="fa fa-youtube"></i></button>
                        <button class="border border-gray-300 rounded-full p-1 transition-colors hover:bg-gray-200 flex items-center justify-center w-8 h-8" ><i class="fa fa-instagram"></i></button>
                    </div>
                </div>
                <div class="">
                    <div class="text-xs font-bold mb-5">Have questions or feedback?<br>Reach out to our support team at</div>
                        <a href="mailto:Contact@fitness.com" class="text-2xl font-semibold tracking-wider">
                        Contact@fitness.com
                        </a>
                    </div>
                <div class="">
                <div class="text-xs font-bold mb-5"> Give us call at</div>
                    <a href="tel:+40675330522" class="text-2xl font-semibold tracking-wider">
                    (406) 753-30522
                    </a>
                </div>
            </div>
            <nav class="flex justify-start p-3 items-center space-x-6 border-b pt-3 max-[450px]:grid max-[450px]:space-x-0 max-[450px]:space-y-3">
                <a href="/" class="text-sm hover:text-gray-900 transition-colors">Home</a>
                <a href="/features" class="text-sm hover:text-gray-900 transition-colors">Features</a>
                <a href="/exercise" class="text-sm hover:text-gray-900 transition-colors">Exercise</a>
                <a href="/about" class="text-sm hover:text-gray-900 transition-colors">About us</a>
                <a href="/apps" class="text-sm hover:text-gray-900 transition-colors">Apps</a>
                <a href="/blog" class="text-sm hover:text-gray-900 transition-colors">Blog</a>
            </nav>
        
            <div class="flex flex-col md:flex-row items-center justify-between text-xs  mt-6 space-y-2 md:space-y-0">
                <span class="text-gray-600">Copyright © 2024 All right resverd</span>
                <div class="flex space-x-4">
                    <a href="/privacy-policy" class="hover:text-gray-900 transition-colors">Privacy Policy</a>
                    <a href="/terms-of-use" class="hover:text-gray-900 transition-colors">Terms of Use</a>
                </div>
            </div>
        </div>
    </footer>
</div>