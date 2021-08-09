<template>
    <div class="product text-left">
    <Header />
            <!-- Breadcrumb Section Begin -->
    <div class="breacrumb-section">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="breadcrumb-text product-more">
                        <router-link to="/"><i class="fa fa-home"></i> Home</router-link>
                        <span>Detail</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Breadcrumb Section Begin -->

    <!-- Product Shop Section Begin -->
    <section class="product-shop spad page-details">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="row">
                        <div class="col-lg-6">
                            <div class="product-pic-zoom">
                                <img class="product-big-img" :src= "default_gambar" alt="" />
                            </div>
                            <div class="product-thumbs">
                                <carousel class="product-thumbs-track ps-slider" :loop="true" :nav="false" :dots="false" :autoplay="true">
                                    <div class="pt" @click="changeImage(thumbs[0])" :class="thumbs[0] == default_gambar ? 'active' : ' ' ">
                                        <img src="img/1b.jpeg" alt="" />
                                    </div>

                                    <div class="pt"  @click="changeImage(thumbs[1])" :class="thumbs[1] == default_gambar ? 'active' : ' ' ">
                                        <img src="img/2b.jpeg" alt="" />
                                    </div>

                                    <div class="pt"  @click="changeImage(thumbs[2])" :class="thumbs[2] == default_gambar ? 'active' : ' ' ">
                                        <img src="img/3b.jpeg" alt="" />
                                    </div>

                                    <div class="pt"  @click="changeImage(thumbs[3])" :class="thumbs[3] == default_gambar ? 'active' : ' ' ">
                                        <img src="img/2b.jpeg" alt="" />
                                    </div>
                                </carousel>
                            </div>
                        </div>
                        <div class="col-lg-6">
                            <div class="product-details">
                                <div class="pd-title">
                                    <span>Bag</span>
                                    <h3>Rotan Bag</h3>
                                </div>
                                <div class="pd-desc">
                                    <p>
                                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, error officia. Rem aperiam laborum voluptatum vel, pariatur modi hic provident eum iure natus quos non a sequi, id accusantium! Autem.
                                    </p>
                                    <p>
                                        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quam possimus quisquam animi, commodi, nihil voluptate nostrum neque architecto illo officiis doloremque et corrupti cupiditate voluptatibus error illum. Commodi expedita animi nulla aspernatur.
                                        Id asperiores blanditiis, omnis repudiandae iste inventore cum, quam sint molestiae accusamus voluptates ex tempora illum sit perspiciatis. Nostrum dolor tenetur amet, illo natus magni veniam quia sit nihil dolores.
                                        Commodi ratione distinctio harum voluptatum velit facilis voluptas animi non laudantium, id dolorem atque perferendis enim ducimus? A exercitationem recusandae aliquam quod. Itaque inventore obcaecati, unde quam
                                        impedit praesentium veritatis quis beatae ea atque perferendis voluptates velit architecto?
                                    </p>
                                    <h4>$495.00</h4>
                                </div>
                                <div class="quantity">
                                    <router-link to="/cart" class="primary-btn pd-cart">Add To Cart</router-link>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <RelatedProduct />
    <!-- Product Shop Section End -->
        <Footer />
    </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
import RelatedProduct from '@/components/RelatedProduct.vue'
import carousel from 'vue-owl-carousel'


export default {
    name: 'product',
    components: {
    Header,
    RelatedProduct,
    Footer,
    carousel
    },
    data() {
        return {
            default_gambar: "img/1b.jpeg",
            thumbs: [
                "img/1b.jpeg",
                "img/2b.jpeg",
                "img/3b.jpeg",
                "img/4b.jpeg",
            ]
        }
    },
    methods: {
        changeImage(urlImage) {
            this.default_gambar = urlImage;
        }
    }
}
</script>

<style>
        .product-thumbs .pt {
        margin-right: 15px;
    }
</style>