<template>
    <!-- Footer -->
    <footer id="footer">
        <div class="container p-0">
            <div class="footer-top row">
                <div class="col-7 d-flex align-items-center justify-content-between">
                    <p class="title-regis">Đăng kí nhận tin</p>
                    <form class="form-send-mail d-flex">
                        <div class="form-group">
                            <label for="email" class="email"><i class="bi bi-envelope"></i></label>
                            <input type="email" id="email" placeholder="Email" required>
                            <button type="submit" class="btn btn-primary btn-send-mail">
                                <i class="bi bi-send me-1"></i>
                                ĐĂNG KÝ
                            </button>
                        </div>
                    </form>
                </div>
                <div class="col-5 d-flex align-items-center justify-content-end">
                    <ul class="social-footer d-flex align-items-center gap-3">
                        <li>
                            <a href="#">
                                <i class="bi bi-tiktok"></i>
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <i class="bi bi-facebook"></i>
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <i class="bi bi-instagram"></i>
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <i class="bi bi-twitter-x"></i>
                            </a>
                        </li>
                    </ul>
                </div>
            </div>

            <div class="line"></div>

            <div class="footer-content row">
                <div class="col-3">
                    <!-- Logo -->
                    <Logo />
                    <div class="information">
                        <p>WD Smart - Điện Thoại Siêu Rẻ, Trao Trọn Yên Tâm.</p>
                        <ul>
                            <li>
                                <i class="bi bi-geo-alt-fill"></i>
                                59A Âu cơ, Phường 14, Quận 11, TP. HCM
                            </li>
                            <li>
                                <i class="bi bi-telephone-fill"></i>
                                0333301536
                            </li>
                            <li>
                                <i class="bi bi-envelope-fill"></i>
                                anhhai282003@gmail.com
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="col-3 tab-link ps-3">
                    <h4>CHÍNH SÁCH</h4>
                    <ul class="ps-3">
                        <li><a href="#">Chính sách bảo hành</a></li>
                        <li><a href="#">Tra cứu bảo hành</a></li>
                        <li><a href="#">Trả góp online</a></li>
                        <li><a href="#">Hướng dẫn thiết lập</a></li>
                        <li><a href="#">Tính năng</a></li>
                    </ul>
                </div>
                <div class="col-3 tab-link ps-3">
                    <h4>LINKS</h4>
                    <ul class="ps-3">
                        <li><a href="#">Tìm kiếm</a></li>
                        <li><a href="#">Giới thiệu</a></li>
                        <li><a href="#">Chính sách đổi trả</a></li>
                        <li><a href="#">Chính sách bảo mật</a></li>
                        <li><a href="#">Điều khoản dịch vụ</a></li>
                        <li><a href="#">Liên hệ</a></li>
                    </ul>
                </div>
                <div class="col-3">
                    <div class="title-footer">
                        <h4>TỔNG ĐÀI HỖ TRỢ</h4>
                    </div>
                    <ul class="footer-support">
                        <li>
                            <span>Gọi mua hàng: </span>
                            <a href="#">0385942049</a>
                            <span>(8h30-21h)</span>
                        </li>
                        <li>
                            <span>Gọi mua hàng: </span>
                            <a href="#">0385942049</a>
                            <span>(8h30-21h)</span>
                        </li>
                        <li>
                            <span>Gọi mua hàng: </span>
                            <a href="#">0385942049</a>
                            <span>(8h30-21h)</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<script setup>
import Logo from './Logo.vue';
</script>