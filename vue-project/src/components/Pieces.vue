<template>
  <div>
    <h1>Hair Piece Plug</h1>
    <div class="pieces">
      <div class="card">
        <div v-for="(piece, index) in pieces" :key="index">
          <h3>{{ piece.name }}</h3>
          <h4>{{ piece.cost }}</h4>
          <img :src="piece.image" />
          <button v-on:click="addItemToCart">Add to Cart</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      pieces: [
        {
          name: "360 Waves",
          cost: "$40,000",
          image:
            "https://i.pinimg.com/originals/56/6a/f3/566af310b855a008dcbfe9a3c80a92d7.jpg",
        },
        {
          name: "540 Waves",
          cost: "$60,000",
          image:
            "https://pbs.twimg.com/ext_tw_video_thumb/1279440058165182464/pu/img/RjMggbo8GBSTCb69.jpg",
        },
        {
          name: "720 Waves",
          cost: "$65,000",
          image:
            "https://cdn.shopify.com/s/files/1/0485/2033/1428/files/720_waves_480x480.jpg?v=1615389155",
        },
        {
          name: "Quiff",
          cost: "$20",
          image:
            "https://lovehairstyles.com/wp-content/uploads/2019/03/quiff-haircut-hairstyle-brown-beard-683x1024.jpg",
        },
        {
          name: "Dreads",
          cost: "$160",
          image:
            "https://i1.sndcdn.com/avatars-ObJgqgPnchE2xGBN-gozVwA-t500x500.jpg ",
        },
        {
          name: "Box Braids",
          cost: "$200",
          image:
            "https://images.squarespace-cdn.com/content/v1/5cda18bc840b16b1970eb444/1620006784089-TLKEEKGEO2F569P65SU5/IMG_9711.JPG?format=750w",
        },
        {
          name: "Two Block",
          cost: "$140",
          image:
            "https://i.pinimg.com/736x/26/35/13/26351360e6a468ef9c89956988185634.jpg",
        },
        {
          name: "Bald",
          cost: "$0.99",
          image:
            "https://www.cameo.com/cdn-cgi/image/fit=cover,format=auto,width=500,height=500/https://cdn.cameo.com/resizer/static/user/avatar-yZlgNegGG.jpg",
        },
        {
          name: "Wolfcut",
          cost: "$250",
          image:
            "https://down-my.img.susercontent.com/file/sg-11134201-22110-deldliwbokjv6f_tn",
        },
        {
          name: "Vegeta",
          cost: "$18000",
          image:
            "https://images.halloweencostumes.com/products/25985/1-1/child-vegeta-wig.jpg",
        },
        {
          name: "Minecraft Dirt Block",
          cost: "$40",
          image:
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQiIlJLa-HNiZPx0g_ykIed1unjC1GHeGwWsw3sSqCCsk96IvYf19IyXCFIxHoxjDCv2apAwAYdrbE&usqp=CAU&ec=48665701",
        },
        {
          name: "Hog Ridaaa",
          cost: "$550",
          image: "http://i.imgur.com/ugQtmZE.jpg ",
        },
        {
          name: "Paintbrush",
          cost: "$40",
          image:
            "https://e1.pxfuel.com/desktop-wallpaper/115/75/desktop-wallpaper-funny-haircuts.jpg",
        },
        {
          name: "Ceiling Fan",
          cost: "$40",
          image:
            "https://fadeawayworld.net/.image/ar_1:1%2Cc_fill%2Ccs_srgb%2Cfl_progressive%2Cq_auto:good%2Cw_1200/MTgwMTMyODA1ODM1MjM2NDc0/joel-embiid-shows-funny-new-haircut-for-birthday.jpg",
        },
        {
          name: "Bob Ross",
          cost: "$100",
          image:
            "https://www.outsideonline.com/wp-content/uploads/2019/05/07/bob-ross-smile_s.jpg?crop=1:1&width=300&enable=upscale",
        },
        {
          name: "Emo",
          cost: "$200",
          image:
            "http://image-cdn.essentiallysports.com/wp-content/uploads/Emo-Logan-Paul.jpg ",
        },
        {
          name: "Goku",
          cost: "$9000",
          image:
            "https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/51a0633c-80b1-45b8-8d22-228c1447efb2/d3ag2y7-4d196068-c93b-42b5-ae61-5749de49bdf5.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzUxYTA2MzNjLTgwYjEtNDViOC04ZDIyLTIyOGMxNDQ3ZWZiMlwvZDNhZzJ5Ny00ZDE5NjA2OC1jOTNiLTQyYjUtYWU2MS01NzQ5ZGU0OWJkZjUuanBnIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.ebZh7wYkqcNgqU4bcCAWaSTkOOwYTvnH6eUA8f5yxU8",
        },
        {
          name: "CLB",
          cost: "$50000",
          image:
            "https://people.com/thmb/zNT1GoL9JROSIyWpi0zOgk04Ph8=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc():focal(599x569:601x571)/drake-1-c6e5d427dd9c40499a7a07e911fc7b9a.jpg",
        },
        {
          name: "Cheeto",
          cost: "$2",
          image:
            "https://nypost.com/wp-content/uploads/sites/2/2022/04/Jam_Press_JMP185735.jpg",
        },
        {
          name: "Mustache",
          cost: "$20",
          image: "https://i.imgflip.com/13sfm6.jpg",
        },
        {
          name: "R9",
          cost: "$20",
          image:
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSnwVecskO5jWp8tg-_EdWXnPnSBRzKq4lB5qkVYI2Itg&usqp=CAU&ec=48665701",
        },
      ],
    };
  },
  methods: {
    addItemToCart(piece) {
      console.log("here", piece);
      this.$emit("addItemToCart", piece);
    },
  },
};
</script>

<style></style>
