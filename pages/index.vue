<template>

    <div class="dropdown-container d-flex mt-3 gap-5 ms-4 ">
        <div class="dropdown">
            <button class="btn btn-primary dropdown-toggle" type="button" id="dropdownMenuButton1"
                data-bs-toggle="dropdown" aria-expanded="false">
                Student: ID
            </button>
            <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
                <li v-for="Product in Products" :key="Product.id"><a class="dropdown-item" href="#">{{ Product.id }}</a>
                </li>
            </ul>
        </div>
        <div class="dropdown">
            <button class="btn btn-secondary dropdown-toggle" type="button" data-bs-toggle="dropdown"
                aria-expanded="false">
                Student: NAME
            </button>
            <ul class="dropdown-menu">
                <li v-for="Product in Products" :key="Product.id"><a class="dropdown-item" href="#">{{
                    Product.name
                }}</a>
                </li>
            </ul>
        </div>
        <div class="dropdown">
            <button class="btn btn-success dropdown-toggle" type="button" data-bs-toggle="dropdown"
                aria-expanded="false">
                Student: AGE
            </button>
            <ul class="dropdown-menu">
                <li v-for="Product in Products" :key="Product.id"><a class="dropdown-item" href="#">{{
                    Product.age
                }}</a>
                </li>
            </ul>
        </div>
        <div class="dropdown">
            <button class="btn btn-info dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
                Student: BLOOD GROUP
            </button>
            <ul class="dropdown-menu">
                <li v-for="Product in Products" :key="Product.id"><a class="dropdown-item" href="#">{{
    Product.Bloodgroup
                }}</a>
                </li>
            </ul>
        </div>
        <div class="dropdown">
            <button class="btn btn-warning dropdown-toggle" type="button" data-bs-toggle="dropdown"
                aria-expanded="false">
                Student: GENDER
            </button>
            <ul class="dropdown-menu">
                <li v-for="Product in Products" :key="Product.id"><a class="dropdown-item" href="#">{{
                    Product.gender
                }}</a>
                </li>
            </ul>
        </div>
        <div class="dropdown">
            <button class="btn btn-danger dropdown-toggle" type="button" data-bs-toggle="dropdown"
                aria-expanded="false">
                Student: SUBJECT
            </button>
            <ul class="dropdown-menu">
                <li v-for="Product in Products" :key="Product.id"><a class="dropdown-item" href="#">{{
                    Product.subject
                }}</a></li>
            </ul>
        </div>
        <div class="dropdown">
            <button class="btn btn-info dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
                Student: Ranking
            </button>
            <ul class="dropdown-menu">
                <li v-for="Product in Products" :key="Product.id"><a class="dropdown-item" href="#">{{
                    Product.ranking
                }}</a></li>
            </ul>
        </div>
    </div>
    <!-- carousels -->
    <div id="carouselExampleInterval" class="carousel slide mt-3" data-bs-ride="carousel">
        <div class="carousel-inner">
            <div class="carousel-item active" data-bs-interval="5000">
                <img src=" https://4kwallpapers.com/images/wallpapers/ducati-panigale-v4-sports-bikes-2022-red-bikes-dark-3840x2160-6952.jpg"
                    class="d-block w-100" alt="...">
            </div>
            <div class="carousel-item" data-bs-interval="4000">
                <img src="https://images.unsplash.com/photo-1635073891744-1e8a4e9cbe98?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8Ym13JTIwczEwMDBycnxlbnwwfHwwfHw%3D&w=1000&q=80"
                    class="d-block w-100" alt="...">
            </div>
            <div class="carousel-item" data-bs-interval="4000">
                <img src="https://wallpaperaccess.com/full/4241928.jpg" class="d-block w-100" alt="...">
            </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleInterval"
            data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleInterval"
            data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
        </button>
    </div>
</template>

<script setup>
import { ref } from "vue";
import data from "../data";
const Products = ref(data);
</script>

<style>

</style>
