<template>
  <div>
    <div
      class="pt-10 pl-[13%] pr-[7%] hidden md:block md:w-[1445px] lg:w-full bg-cover"
      style="background-image: url('/images/bg-seakun.png')"
    >
      <Navbar />
      <IntroSection />
    </div>
    <div class="bg-[#68BDFE] md:hidden w-full bg-cover">
      <Navbar />
      <IntroSection />
    </div>
    <div class="md:pl-[13%]">
      <PortofilioSection />
    </div>
    <div>
      <BenefitSection />
    </div>
    <div class=" md:pl-[13%] pl-[6%] md:pr-[5%]">
      <InformationBanner />
    </div>
    <div class="max-md:pl-[3%]  md:pl-[13%] md:pr-[7%]">
      <Product />
    </div>
    <div class="md:pl-[13%] max-md:mx-[6%] md:pr-[10%]">
      <ProductNonDigital />
    </div>
    <div class="bg-[#F4BD42]">
      <HowToSubscribe />
    </div>
    <div class="bg-[#FFF8EA]">
      <PaymentMethod />
    </div>
    <div class="">
      <Partner />
    </div>
    <div class=" bg-[#2D2D2D]">
      <Testimoni />
    </div>
    <div class="lg:pl-[13%] max-md:px-6 lg:pr-[10%]">
      <UserSeakun />
    </div>
    <div class=" bg-[#00BA88]">
      <DownloadApp />
    </div>
    <div class="">
      <FaqSection />
    </div>
    <div class="">
      <Warning />
    </div>
    <div class="lg:mb-[15%]">
      <Cooperation />
    </div>
    <div class="lg:pl-[10%]">
      <Footer />
    </div>
  </div>
</template>

<script>
import Navbar from "~/components/Navbar";
import IntroSection from "~/components/IntroSection";
import PortofilioSection from "~/components/PortofilioSection";
import BenefitSection from "~/components/BenefitSection";
import InformationBanner from "~/components/InformationBanner";
import Product from "~/components/Product";
import ProductNonDigital from "~/components/ProductNonDigital";
import HowToSubscribe from "~/components/HowToSubscribe";
import PaymentMethod from "~/components/PaymentMethod";
import UserSeakun from "~/components/UserSeakun";
import DownloadApp from "~/components/DownloadApp";
import FaqSection from "~/components/FaqSection";
import Warning from "~/components/Warning";
import Cooperation from "~/components/Cooperation";
import Footer from "~/components/Footer";
export default {
  components: {
    Navbar,
    IntroSection,
    PortofilioSection,
    BenefitSection,
    InformationBanner,
    Product,
    ProductNonDigital,
    HowToSubscribe,
    PaymentMethod,
    UserSeakun,
    DownloadApp,
    FaqSection,
    Warning,
    Cooperation,
    Footer,
  },
};
</script>
