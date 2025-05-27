<template>
  <div >
    <div class=" pt-10 pl-[13%] pr-[7%] bg-cover w-full" style="background-image: url('/images/bg-seakun.png');">
      <Navbar/>
      <IntroSection/>
    </div>
    <div class="pl-[13%]">
      <PortofilioSection/>
    </div>
    <BenefitSection/>
    <div class="pl-[13%] pr-[5%]">
      <InformationBanner/>
    </div>
    <div class="pl-[13%] pr-[7%]">
      <CardProduct/>
    </div>
    </div>
</template>

<script>
import Navbar from "~/components/Navbar";
import IntroSection from "~/components/IntroSection";
import PortofilioSection from "~/components/PortofilioSection";
import BenefitSection from "~/components/BenefitSection";
import InformationBanner from "~/components/InformationBanner";
import CardProduct from "~/components/CardProduct";
export default {
    components :{
        Navbar,
        IntroSection,
        PortofilioSection,
        BenefitSection,
        InformationBanner,
        CardProduct,
    }
}
</script>