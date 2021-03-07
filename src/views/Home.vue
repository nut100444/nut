<template>
  <div class="home">
    <div>
      <b-carousel
        id="carousel-fade"
        style="text-shadow: 0px 0px 2px #000 "
        fade
        indicators
        img-width="1024"
        img-height="250"
      >
        <b-carousel-slide
        style="height:30rem"
          
          img-src="https://s3.ap-southeast-1.amazonaws.com/store-front.arifootballstore.com/arifootball/cms/media/BLACKPACK-HP%20%281%29.jpg"
        ></b-carousel-slide>
        <b-carousel-slide
        style="height:30rem"
          
          img-src="https://s3.ap-southeast-1.amazonaws.com/store-front.arifootballstore.com/arifootball/cms/media/COPA%20SENSE%20HP.jpg"
        ></b-carousel-slide>
        <b-carousel-slide
        style="height:30rem"
         
          img-src="https://s3.ap-southeast-1.amazonaws.com/store-front.arifootballstore.com/arifootball/cms/media/SPECTRUM%20-HP.jpg"
        ></b-carousel-slide>
      </b-carousel>
    </div>
    <div class="row">
      <HelloWorld
        class="col-3"
        v-for="(item, index) in nun"
        :key="index"
        :img="item.img"
        :name="item.name"
        :price="item.price"
        @Order="menuorder"
      />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
  },
  data() {
    return {
      select: [],
      nun: [
        {
          img:
            "https://cdn.arifootballstore.com/catalog/product/cache/image/beff4985b56e3afdbeabfc89641a4582/n/i/nike_vapor_14_elite_fg_-_bright_crimson_metallic_silver_cq7635-600__00.jpg?w=400",
          name: "NIKE MERCURIAL VAPOR 14 ELITE FG - BRIGHT CRIMSON/METALLIC SILVER",
          price: 8500,
        },
        {
          img:
            "https://cdn.arifootballstore.com/catalog/product/cache/image/beff4985b56e3afdbeabfc89641a4582/n/i/nike_phantom_gt_elite_fg_-_photo_blue_metallic_silver-rage_green_-_ck8439-400__00.jpg?w=400",
          name: "NIKE PHANTOM GT ELITE FG - PHOTO BLUE/METALLIC SILVER-RAGE GREEN",
          price: 8500,
        },
        {
          img:
            "https://cdn.arifootballstore.com/catalog/product/cache/image/beff4985b56e3afdbeabfc89641a4582/n/i/nike_legend_8_elite_fg_-_platinum_tint_rage_green_at5293-030__00.jpg?w=400",
          name: "NIKE TIEMPO LEGEND 8 ELITE FG - PLATINUM TINT/RAGE GREEN",
          price: 7900,
        },
        {
          img:
            "https://cdn.arifootballstore.com/catalog/product/cache/image/beff4985b56e3afdbeabfc89641a4582/n/i/nike_vapor_14_elite_fg_-_black_cyber-off_noir_-_cq7635-090_00.jpg?w=400",
          name: "NIKE MERCURIAL VAPOR 14 ELITE FG - BLACK/CYBER-OFF NOIR",
          price: 8500,
        },
        {
          img:
            "https://cdn.arifootballstore.com/catalog/product/cache/image/beff4985b56e3afdbeabfc89641a4582/a/d/adidas_copa_sense.1_fg_-_cblack_grefiv_grefiv_fw6498__00.jpg?w=400",
          name: "ADIDAS COPA SENSE.1 FG - CORE BLACK/GREY FIVE",
          price: 7300,
        },
        {
          img:
            "https://cdn.arifootballstore.com/catalog/product/cache/image/beff4985b56e3afdbeabfc89641a4582/a/d/adidas_predator_freak_.1_l_fg_-_cblack_grefou_ftwwht_fy1028__00.jpg?w=400",
          name: "ADIDAS PREDATOR FREAK.1 L FG - CORE BLACK/GREY FOUR",
          price: 7800,
        },
        {
          img:
            "https://cdn.arifootballstore.com/catalog/product/cache/image/beff4985b56e3afdbeabfc89641a4582/a/d/adidas_predator_freak_.1_l_fg_-_cblack_ftwwht_syello_fy0745__00.jpg?w=400",
          name: "ADIDAS PREDATOR FREAK.1 L FG - CORE BLACK/SOLAR YELLOW",
          price: 7800,
        },
        {
          img:
            "https://cdn.arifootballstore.com/catalog/product/cache/image/beff4985b56e3afdbeabfc89641a4582/a/d/adidas_nemeziz_.1_fg_-_cblack-cblack-cblack_fw7422__00.jpg?w=400",
          name: "ADIDAS NEMEZIZ .1 FG - CORE BLACK/CORE BLACK",
          price: 7800,
        },
      ],
    };
  },
  methods: {
    menuorder(value) {
      this.$emit("Order", value);
    },
  },
};
</script>
