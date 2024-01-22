<script setup>
import { Head, Link } from '@inertiajs/vue3';

defineProps({
    canLogin: {
        type: Boolean,
    },
    canRegister: {
        type: Boolean,
    },
    laravelVersion: {
        type: String,
        required: true,
    },
    asset: {
        type: String,
        required: true,
    },
    phpVersion: {
        type: String,
        required: true,
    },

});

</script>

<template>
    <Head title="Home" />

    <div>

    <nav>
        <div class=" main-nav d-flex justify-content-around navbar navbar-expand-lg navbar-light bg-white ">
            <section class="d-flex">
                <a class="login navbar-brand btn btn-main text-white d-none d-lg-block" href="#" data-toggle="modal"
                    data-target="#loginModal">تسجيل الدخول</a>
                <img  :src="assetPath(asset,'cart-btn.png')"  class="cart d-inline-block" alt="cart">

            </section>
            <section class="">
                <figure class=" logo ">
                    <img :src="assetPath(asset,'log-removebg-preview.png')" class="w-100 d-inline-block m-0 p-0" alt="cart">
                </figure>
            </section>
            <section>
                <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav"
                    aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>

            </section>
            <div class="collapse navbar-collapse " id="navbarNav">

                <ul class="navbar-nav ml-auto">

                    <li class="nav-item">
                        <a class="nav-link main-text-color" href="#">من نحن</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link main-text-color" href="#">الاسئلة الشائعة</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link main-text-color" href="#">المزادات</a>
                    </li>

                    <li class="nav-item">
                        <a class="nav-link main-text-color" href="#">الرئيسية</a>
                    </li>
                    <li class="nav-item d-lg-none">
                        <a class="nav-link btn btn-main text-white" href="#" data-toggle="modal"
                            data-target="#loginModal">تسجيل
                            الدخول</a>
                    </li>
                </ul>
            </div>
        </div>



    </nav>
    <div class="container">

        <!-- Bootstrap Navigation Bar -->


        <div class="modal fade" id="loginModal" tabindex="-1" role="dialog" aria-labelledby="loginModalLabel"
            aria-hidden="true">
            <div class="modal-dialog" role="document">
                <div class="modal-content">
                    <div class="modal-header">
                        <h5 class="modal-title main-text-color" id="loginModalLabel">تسجيل الدخول</h5>
                        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                            <span aria-hidden="true">&times;</span>
                        </button>
                    </div>
                    <div class="modal-body">
                        <!-- Add your login form here -->
                        <form>
                            <div class="form-group">
                                <label for="username">اسم المستخدم</label>
                                <input type="text" class="form-control" id="username" placeholder="ادخل اسم المستخدم">
                            </div>
                            <div class="form-group">
                                <label for="password">كلمة المرور</label>
                                <input type="password" class="form-control" id="password"
                                    placeholder="ادخل كلمة المرور">
                            </div>
                            <button type="submit" class="btn btn-main">تسجيل الدخول</button>
                        </form>
                    </div>
                </div>
            </div>
        </div>

        <div class=" mt-5 main">


            <!-- Your content goes here -->

            <main class=" rounded">
                <p class="h1 text-right sm-position-absolute ">المزادات</p>


                <ul class="list-unstyled d-flex flex-nowrap justify-content-end">

                    <li class="">
                        <a class="main-text-color" href="#">منتهى +99 </a>
                    </li>
                    <li class="">
                        <a class="main-text-color" href="#">قادم 10</a>
                    </li>
                    <li class="">
                        <a class="main-text-color" href="#">جاري 4</a>
                    </li>
                    <li class="">
                        <a class="main-text-color" href="#">الكل 14</a>
                    </li>


                </ul>
            </main>

        </div>
        <div class=" my-3">
            <div class="row d-flex justify-content-end p-3 sort-icons">
                <i class="fa-solid fa-bars m-2"></i>
                <i class="fa-solid fa-table-cells-large m-2"></i>
                <i class="fa-solid fa-table-cells m-2"></i>
                <!-- <figure class="p-3">
                    <img :src="assetPath(asset,"menu-burger.png")" class="sort-icon" alt="Card Image">

                </figure>
                <figure class="p-3">
                    <img :src="assetPath(asset,"dots-menu-svgrepo-com.svg" class="sort-icon" alt="Card Image">
                </figure> -->
            </div>
        </div>
        <div class=" text-align-end">
            <div class="row ">


                <div class="col-lg-4 my-3">
                    <div class="card">
                        <div class="card-img-info">

                            <div class="btn btn-dis"> <i class="fa-solid fa-eye"></i> عرض </div>
                            <i class="fa-solid fa-star star"></i>
                            <!-- <img :src="assetPath(asset,"star.svg" class="star" alt="Star SVG"> -->

                        </div>
                        <img :src="assetPath(asset,'download.jpeg')" class="card-img-top" alt="Card Image">
                        <div class="rounded card-pop">

                            <div class=""> انتهى المزاد </div>
                            <!-- <img :src="assetPath(asset,"star.svg" class="star" alt="Star SVG"> -->

                        </div>
                        <div class="card-body ">
                            <div class="card-h mb-3 d-flex justify-content-center">
                                <!-- <button class="btn card-btn-info ">التفصيل</button> -->
                                <h5 class="card-title text-success">جوال ايفون 14 برو مكس</h5>

                            </div>
                            <!-- <div class="card-h mb-3 d-flex justify-content-between">
                                <button class="btn card-btn-info">التفصيل</button>
                                <h5 class="card-title text-success">جوال ايفون 14 برو مكس</h5>

                            </div> -->
                            <div class="card-b mb-3 d-flex justify-content-end">
                                <input type="text" class="card-input rounded">
                                <p class="w-50">مبلغ ترسية المزاد</p>

                            </div>
                            <div class="card-b mb-3 d-flex justify-content-end">
                                <input type="text" class="card-input rounded">
                                <p class="w-50">المزاود</p>

                            </div>
                            <div class="card-h mb-3 d-flex justify-content-between">
                                <button class="btn card-btn-info">لوحة المزايدة</button>
                                <button class="btn card-btn-info">زاود</button>

                            </div>

                        </div>
                    </div>
                </div>
                <div class="col-lg-4 my-3">
                    <div class="card">
                        <div class="card-img-info">

                            <div class="btn btn-dis"> <i class="fa-solid fa-eye"></i> عرض </div>
                            <i class="fa-solid fa-star star"></i>
                            <!-- <img :src="assetPath(asset,"star.svg" class="star" alt="Star SVG"> -->

                        </div>
                        <img :src="assetPath(asset,'download.jpeg')" class="card-img-top" alt="Card Image">
                        <div class="rounded card-pop">

                            <div class=""> انتهى المزاد </div>
                            <!-- <img :src="assetPath(asset,"star.svg" class="star" alt="Star SVG"> -->

                        </div>
                        <div class="card-body ">
                            <div class="card-h mb-3 d-flex justify-content-center">
                                <h5 class="card-title text-success">جوال ايفون 14 برو مكس</h5>

                            </div>
                            <div class="card-b mb-3 d-flex justify-content-end">
                                <input type="text" class="card-input rounded">
                                <p class="w-50">مبلغ ترسية المزاد</p>

                            </div>
                            <div class="card-b mb-3 d-flex justify-content-end">
                                <input type="text" class="card-input rounded">
                                <p class="w-50">المزاود</p>

                            </div>
                            <div class="card-h mb-3 d-flex justify-content-between">
                                <button class="btn card-btn-info">منتهي</button>

                            </div>

                        </div>
                    </div>
                </div>
                <div class="col-lg-4 my-3">
                    <div class="card">
                        <div class="card-img-info">

                            <div class="btn btn-dis"> <i class="fa-solid fa-eye"></i> عرض </div>
                            <i class="fa-solid fa-star star"></i>
                            <!-- <img :src="assetPath(asset,"star.svg" class="star" alt="Star SVG"> -->

                        </div>
                        <img :src="assetPath(asset,'download.jpeg')" class="card-img-top" alt="Card Image">
                        <div class="rounded card-pop">

                            <div class=""> انتهى المزاد </div>
                            <!-- <img :src="assetPath(asset,"star.svg" class="star" alt="Star SVG"> -->

                        </div>
                        <div class="card-body ">
                            <div class="card-h mb-3 d-flex justify-content-center">
                                <h5 class="card-title text-success">جوال ايفون 14 برو مكس</h5>

                            </div>
                            <div class="card-b mb-3 d-flex justify-content-end">
                                <input type="text" class="card-input rounded">
                                <p class="w-50">مبلغ ترسية المزاد</p>

                            </div>
                            <div class="card-b mb-3 d-flex justify-content-end">
                                <input type="text" class="card-input rounded">
                                <p class="w-50">المزاود</p>

                            </div>
                            <div class="card-h mb-3 d-flex justify-content-between">
                                <button class="btn card-btn-info">منتهي</button>

                            </div>

                        </div>
                    </div>
                </div>





            </div>
        </div>
        <div class=" my-5  d-flex justify-content-end flex-column">

            <p class="h2 text-right">زاود : وكن الفائز</p>
            <p class="h5 text-right text-secondary text-align-end">خطوات المشاركة والفوز</p>

            <ul class="list-unstyled d-flex flex-wrap justify-content-around w-100 py-5 ">
                <li class="text-center">
                    <p>......................... 3</p>
                    <a class="nav-link text-secondary" href="#"> المزايدة والفوز </a>
                </li>
                <li class="">
                    <p>......................... 2</p>
                    <a class="nav-link text-secondary" href="#"> الاشتراك </a>
                </li>
                <li class=" ">
                    <p>......................... 1</p>
                    <a class="nav-link text-secondary" href="#"> التسجيل </a>
                </li>

            </ul>
            <ul class="list-unstyled d-flex flex-wrap justify-content-around w-100 py-5 ">

                <li class="text-center">
                    <a class="nav-link text-secondary" href="#"> من نحن</a>
                </li>
                <li class="">
                    <a class="nav-link text-secondary" href="#"> الروابط </a>
                </li>
                <li class=" ">
                    <a class="nav-link text-secondary" href="#"> التواصل </a>
                </li>
                <li class="text-center">
                    <img :src="assetPath(asset,'log-removebg-preview.png')" class="w-100 d-inline-block m-0 p-0 logo" alt="">
                </li>
            </ul>

            <div class="footer-icons d-flex justify-content-between">

                <div class="payment">
                    <iconify-icon icon="simple-icons:applepay"></iconify-icon>
                    <iconify-icon icon="logos:visa"></iconify-icon>
                    <iconify-icon icon="logos:mastercard"></iconify-icon>
                </div>
                <div class="social">
                    <iconify-icon icon="akar-icons:linkedin-fill"></iconify-icon>
                    <iconify-icon icon="mdi:youtube"></iconify-icon>
                    <iconify-icon icon="pajamas:x"></iconify-icon>
                </div>
            </div>
        </div>

        <!-- <figure>
            <img :src="assetPath(asset,"Screenshot from 2024-01-12 00-59-29.png")" class="card-img-top h-100 cover" alt="Card Image">

        </figure> -->

    </div>

    <footer>
        <section class="bg-footer-end text-center">
            <p>جميع الحقوق محفوظة : بموجب براءة اختراع فكرية في الهيئة السعودية للملكية الفكرية رقم 103864100003
                بتاريخ 2023/11/17, ردمك 3-85-12-7963-971.</p>
        </section>
    </footer>
    <!-- Link Bootstrap JS and Popper.js -->

</div>
</template>

<style>
.bg-dots-darker {
    background-image: url("data:image/svg+xml,%3Csvg width='30' height='30' viewBox='0 0 30 30' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M1.22676 0C1.91374 0 2.45351 0.539773 2.45351 1.22676C2.45351 1.91374 1.91374 2.45351 1.22676 2.45351C0.539773 2.45351 0 1.91374 0 1.22676C0 0.539773 0.539773 0 1.22676 0Z' fill='rgba(0,0,0,0.07)'/%3E%3C/svg%3E");
}
@media (prefers-color-scheme: dark) {
    .dark\:bg-dots-lighter {
        background-image: url("data:image/svg+xml,%3Csvg width='30' height='30' viewBox='0 0 30 30' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M1.22676 0C1.91374 0 2.45351 0.539773 2.45351 1.22676C2.45351 1.91374 1.91374 2.45351 1.22676 2.45351C0.539773 2.45351 0 1.91374 0 1.22676C0 0.539773 0.539773 0 1.22676 0Z' fill='rgba(255,255,255,0.07)'/%3E%3C/svg%3E");
    }
}

</style>
<script>
export default {
          methods:{
            assetPath(asset,urlPath){
                         return  `${asset}/${urlPath}`;
                     }
                 }
            }
 </script>
