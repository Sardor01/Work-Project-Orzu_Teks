<template>
  <div class="home">
    <Header />
    <ShowCaseSlider />
    <AboutUs />
    <Manufacture />
    <Uniform />
    <Collection />
    <Partners />
    <Contact />
    <Footer />
  </div>
</template>

<script>
  // @ is an alias to /src
  import Header from "@/shells/Header";
  import Contact from "@/shells/Contact";
  import Footer from "@/shells/Footer";

  import ShowCaseSlider from "@/components/Home/ShowCaseSlider";
  import AboutUs from "@/components/Home/AboutUs";
  import Manufacture from "@/components/Home/Manufacture";
  import Uniform from "@/components/Home/Uniform";
  import Collection from "@/components/Home/Collection";
  import Partners from "@/components/Home/Partners";

  export default {
    name: "Home",
    components: {
      Header,
      ShowCaseSlider,
      AboutUs,
      Manufacture,
      Uniform,
      Collection,
      Partners,
      Contact,
      Footer,
    },
  };
</script>
