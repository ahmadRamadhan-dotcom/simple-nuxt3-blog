<template>
  <div class="home">
    <Header />
    <main>
      <Hero />
      <div
        class="mt-16 grid place-content-center place-items-center lg:place-items-start gap-8 lg:gap-16 xl:gap-24"
      >
        <div
          class="w-[90%] sm:w-[600px] md:w-[740px] lg:w-[1000px] xl:w-[1250px] 2xl:w-[1500px] min-h-[10em] md:h-[46em] lg:h-[55em] 2xl:min-h-[62em] md:col-span-2 mb-9"
        >
          <a href="#">
            <img
              id="cover_image"
              src="https://res.cloudinary.com/dk7urhntn/image/upload/v1669215233/cover_1_qsb7o5.jpg"
              alt=""
            />
            <p
              id="title"
              class="block md:hidden text-4xl lg:text-[44px] font-normal mt-7"
            >
              Dynamic Routing and Static Generation
            </p>
          </a>
          <div class="md:grid md:grid-cols-2 md:gap-10 md:mt-10">
            <div class="">
              <p id="title" class="hidden md:block text-4xl font-normal mt-7">
                Dynamic Routing and Static Generation
              </p>
              <p id="date" class="font-normal mt-5 text-lg">March 16, 2020</p>
            </div>
            <div>
              <p id="short_desc" class="text-lg mt-5">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
                eiusmod tempor incididunt ut labore et dolore magna aliqua.
                Praesent elementum facilisis leo vel fringilla est ullamcorper
                eget. At imperdiet dui accumsan sit amet nulla facilities morbi
                tempus.
              </p>
              <div id="author" class="flex items-center gap-4 mt-3">
                <img
                  id="author_image"
                  src="https://res.cloudinary.com/dk7urhntn/image/upload/v1669215355/jj_ffnzy8.jpg"
                  alt="author_image"
                  class="h-12 rounded-full"
                />
                <p id="author_name" class="font-bold text-xl">JJ Kasper</p>
              </div>
            </div>
          </div>
        </div>
        <!-- <p class="text-[44px] w-[90%] sm:w-[600px] font-bold">More Stories</p> -->
        <div
          class="w-[90%] mb-14 sm:w-[600px] md:w-[340px] lg:w-[450px] xl:w-[570px] 2xl:w-[700px] min-h-[10em] md:min-h-[20em]"
        >
          <a href="#">
            <img
              id="cover_image"
              src="https://res.cloudinary.com/dk7urhntn/image/upload/v1669213936/cover_ffb8zn.jpg"
              alt="cover_image"
            />
            <p id="title" class="text-[30px] font-normal mt-7">
              Learn How to Pre-render Pages Using Static Generation with Next.js
            </p>
          </a>
          <p id="date" class="font-normal mt-5 text-lg">March 16, 2020</p>
          <p id="short_desc" class="text-lg mt-5">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Praesent
            elementum facilisis leo vel fringilla est ullamcorper eget. At
            imperdiet dui accumsan sit amet nulla facilities morbi tempus.
          </p>
          <div id="author" class="flex items-center gap-4 mt-3">
            <img
              id="author_image"
              src="https://res.cloudinary.com/dk7urhntn/image/upload/v1669214336/tim_vzzb5c.jpg"
              alt="author_image"
              class="h-12 rounded-full"
            />
            <p id="author_name" class="font-bold text-xl">Tim Neutkens</p>
          </div>
        </div>
        <div
          class="w-[90%] sm:w-[600px] md:w-[340px] lg:w-[450px] xl:w-[570px] 2xl:w-[700px] min-h-[10em] md:h-[46em]"
        >
          <a href="#">
            <img
              id="cover_image"
              src="https://res.cloudinary.com/dk7urhntn/image/upload/v1669214731/cover_hgm8pk.jpg"
              alt="cover_image"
            />
            <p id="title" class="text-[30px] font-normal mt-7">
              Preview Mode for Static Generation
            </p>
          </a>
          <p id="date" class="font-normal mt-5 text-lg">March 16, 2020</p>
          <p id="short_desc" class="text-lg mt-5">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Praesent
            elementum facilisis leo vel fringilla est ullamcorper eget. At
            imperdiet dui accumsan sit amet nulla facilities morbi tempus.
          </p>
          <div id="author" class="flex items-center gap-4 mt-3">
            <img
              id="author_image"
              src="https://res.cloudinary.com/dk7urhntn/image/upload/v1669214765/joe_ua6eux.jpg"
              alt="author_image"
              class="h-12 rounded-full"
            />
            <p id="author_name" class="font-bold text-xl">Joe Haddad</p>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>
