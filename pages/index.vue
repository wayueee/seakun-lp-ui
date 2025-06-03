<template>
  <div >
    <div class=" pt-10 pl-[13%] pr-[7%] hidden md:block bg-cover" style="background-image: url('/images/bg-seakun.png');">
      <Navbar/>
      <IntroSection/>
    </div>
    <div class="bg-[#68BDFE] md:hidden w-[360px] h-[770px]" style="background-image: url('/images/bg-seakun-mobile.png');">
      <Navbar/>
      <IntroSection/>
    </div>
    <div class="hidden md:block pl-[13%]">
      <PortofilioSection/>
    </div>
    <BenefitSection/>
    <div class="hidden md:block pl-[13%] pr-[5%]">
      <InformationBanner/>
    </div>
    <div class="hidden md:block pl-[13%] pr-[7%]">
      <Product/>
    </div>
    <div  class="hidden md:block pl-[13%] pr-[10%]">
      <ProductNonDigital/>
    </div>
    <div class="hidden md:block bg-[#F4BD42]">
      <HowToSubscribe/>
    </div>
    <div class="hidden md:block bg-[#FFF8EA]">
      <PaymentMethod />
    </div>
    <div class="hidden md:block">
      <Partner/>
    </div>
    <div class="hidden md:block bg-[#2D2D2D]">
        <Testimoni/>
    </div>
    <div class="hidden md:block pl-[13%] pr-[10%]">
      <UserSeakun/>
    </div>
    <div class="hidden md:block bg-[#00BA88]">
      <DownloadApp/>
    </div>
    <div class="hidden md:block ">
      <FaqSection/>
    </div>
    <div class="hidden md:block ">
      <Warning/>
    </div>
    <div class="hidden md:block pl-[3%]">
      <Footer/>
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
import Footer from "~/components/Footer";
export default {
    components :{
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
        Footer,
    }
}
</script>