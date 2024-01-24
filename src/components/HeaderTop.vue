<template>
    <div class="header-top d-flex align-items-center">
        <div class="container p-0">
            <div class="row d-flex align-items-center">
                <!-- Logo -->
                <Logo />
                <!-- Search -->
                <div class="col-4 header-search p-0">
                    <form id="formSearch">
                        <div class="form-group">
                            <label for="header-search-input" hidden="hidden"></label>
                            <input type="text" class="form-control header-search-input" id="header-search-input" placeholder="Nhập tìm kiếm...">
                        </div>
                        <button type="button" class="btn btn-primary btn-search" onclick="searchProduct()">
                            <i class="bi bi-search"></i>
                        </button>
                    </form>
                </div>
                <!-- Actions -->
                <div class="col-5 group-icon-header ps-3">
                    <ul class="list-icon-header d-flex align-items-center justify-content-between">
                        <li class="item">
                            <a href="tel:033301536" class="item-link text-white d-flex align-items-center">
                                <span class="icon"><i class="bi bi-telephone-forward"></i></span>
                                <span class="text">
                                Hotline
                                <span class="small-text d-block">0333301536</span>
                            </span>
                            </a>
                        </li>
                        <li class="item item-dropdown" @click="showDropdown('ddownStoreAddress')">
                            <div class="header-store block d-flex align-items-center">
                                <span class="icon"><i class="bi bi-geo-alt"></i></span>
                                <span class="text">
                                    Hệ thống
                                    <span class="small-text d-flex align-items-center">
                                        cửa hàng
                                        <i class="bi bi-chevron-down ms-1"></i>
                                    </span>
                                </span>
                                <!-- Drop down -->
                                <div v-if="listDropDown.ddownStoreAddress" @click.stop="" class="header-action_dropdown bg-grey-opacity header-store_dropdown">
                                    <div class="header-dropdown_content">
                                        <div class="icon-close" @click="closeDropdown('ddownStoreAddress')">
                                            <i class="bi bi-x"></i>
                                        </div>
                                        <p class="title">Tìm cửa hàng gần bạn</p>
                                        <div class="d-flex align-items-center justify-content-between gap-2 mt-3">
                                            <select class="form-select select">
                                                <option selected>Chọn tỉnh/thành phố</option>
                                                <option value="1">Hà Nội</option>
                                                <option value="2">Hồ Chí Minh</option>
                                            </select>

                                            <select class="form-select select">
                                                <option selected>Chọn Quận/huyện</option>
                                            </select>
                                        </div>
                                        <div class="address-count mt-4">
                                            <div class="address-detail">
                                                <ul class="address-link">
                                                    <li class="item">
                                                        <a href="#" class="infor">
                                                            <b>Hồ Chí Minh - Wanda CN Thủ Đức</b>
                                                            <span>47 Thống Nhất, Phường Bình Thọ, Quận Thủ Đức</span>
                                                            <span class="phoneNumber d-flex align-items-baseline">
                                                                <i class="bi bi-phone"></i>
                                                                <span class="ms-1">0123456789</span>
                                                            </span>
                                                            <span>Thời gian hoạt động: 9:00 - 21:00</span>
                                                        </a>
                                                        <a href="#" class="infoLocation d-flex align-items-baseline gap-1">
                                                            <i class="bi bi-arrow-bar-right"></i>
                                                            <span>Chỉ đường</span>
                                                        </a>
                                                    </li>

                                                    <li class="item">
                                                        <a href="#" class="infor">
                                                            <b>Hồ Chí Minh - Wanda CN Thủ Đức</b>
                                                            <span>47 Thống Nhất, Phường Bình Thọ, Quận Thủ Đức</span>
                                                            <span class="phoneNumber d-flex align-items-baseline">
                                                                <i class="bi bi-phone"></i>
                                                                <span class="ms-1">0123456789</span>
                                                            </span>
                                                            <span>Thời gian hoạt động: 9:00 - 21:00</span>
                                                        </a>
                                                        <a href="#" class="infoLocation d-flex align-items-baseline gap-1">
                                                            <i class="bi bi-arrow-bar-right"></i>
                                                            <span>Chỉ đường</span>
                                                        </a>
                                                    </li>

                                                    <li class="item">
                                                        <a href="#" class="infor">
                                                            <b>Hồ Chí Minh - Wanda CN Thủ Đức</b>
                                                            <span>47 Thống Nhất, Phường Bình Thọ, Quận Thủ Đức</span>
                                                            <span class="phoneNumber d-flex align-items-baseline">
                                                                <i class="bi bi-phone"></i>
                                                                <span class="ms-1">0123456789</span>
                                                            </span>
                                                            <span>Thời gian hoạt động: 9:00 - 21:00</span>
                                                        </a>
                                                        <a href="#" class="infoLocation d-flex align-items-baseline gap-1">
                                                            <i class="bi bi-arrow-bar-right"></i>
                                                            <span>Chỉ đường</span>
                                                        </a>
                                                    </li>
                                                </ul>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </li>
                        <li class="item item-dropdown" @click="showDropdown('ddownLogin')">
                            <div class="block header-login d-flex align-items-center">
                                <span class="icon"><i class="bi bi-person-fill"></i></span>
                                <span class="text">
                                    Đăng nhập
                                    <span class="small-text d-flex align-items-center">
                                        Đăng ký
                                        <i class="bi bi-chevron-down ms-1"></i>
                                    </span>
                                </span>
                                <!-- Drop down -->
                                <div v-if="listDropDown.ddownLogin" @click.stop="" class="header-action_dropdown bg-grey-opacity">
                                    <div class="header-dropdown_content header-dropdown_login">
                                        <div class="icon-close" @click="closeDropdown('ddownLogin')">
                                            <i class="bi bi-x"></i>
                                        </div>
                                        <p class="title">Đăng nhập tài khoản</p>
                                        <p class="desc">Nhập email và mật khẩu của bạn</p>
                                        <form class="header-form_login">
                                            <div class="mb-2">
                                                <input type="email" class="form-control" id="email-login" required placeholder="Email">
                                            </div>
                                            <div class="mb-2">
                                                <input type="password" class="form-control" id="password-login" required placeholder="Password">
                                            </div>
                                            <button type="submit" class="btn btn-login">Đăng nhập</button>
                                        </form>
                                        <span class="create-account d-block">
                                            Khách hàng mới?
                                            <a href="#">Tạo tài khoản</a>
                                        </span>
                                        <span class="forgot-account d-block">
                                            Quên mật khẩu?
                                            <a href="#">Khôi phục mật khẩu</a>
                                        </span>
                                    </div>
                                </div>
                            </div>
                        </li>
                        <li class="item item-dropdown" @click="showDropdown('ddownCart')">
                            <div class="cart">
                                <button type="button" class="btn btn-primary d-flex align-items-center cart-btn">
                                    <span class="icon"><i class="bi bi-cart"></i></span>
                                    <span class="text">Giỏ hàng</span>
                                </button>
                                <!-- Drop down -->
                                <div v-if="listDropDown.ddownCart" @click.stop="" class="header-action_dropdown bg-grey-opacity header-cart_dropdown">
                                    <div class="header-dropdown_content header-dropdown_login">
                                        <div class="icon-close" @click="closeDropdown('ddownCart')">
                                            <i class="bi bi-x"></i>
                                        </div>
                                        <p class="title">Giỏ hàng</p>
                                        <div class="mini_cart_header text-center py-2">
                                            <i class="bi bi-cart2"></i>
                                            <p>Hiện chưa có sản phẩm</p>
                                        </div>
                                        <hr class="text-dark mb-1" />
                                        <div class="cart-total d-flex align-items-baseline justify-content-between">
                                            <span class="text">TỔNG TIỀN:</span>
                                            <span class="prices">0₫</span>
                                        </div>
                                        <div class="actions d-flex align-items-center justify-content-between py-2">
                                            <a href="#" class="btn btn-primary">XEM GIỎ HÀNG</a>
                                            <a href="#" class="btn btn-outline-primary">THANH TOÁN</a>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
import { ref } from 'vue';
// Component
import Logo from './Logo.vue';

const $emits = defineEmits(['handle-modal']);

// List dropdown header
let listDropDown = ref({
    'ddownStoreAddress': false,
    'ddownLogin': false,
    'ddownCart': false
});

// Handle show dropdown header
function showDropdown(dropDownName) {
    for(let dropDownItem in listDropDown.value) {
        if(dropDownItem === dropDownName) {
            listDropDown.value[dropDownName] = !listDropDown.value[dropDownName];
            // Handle emit event to components/Header.vue
            $emits('handle-modal', listDropDown.value[dropDownName]);
        } else {
            listDropDown.value[dropDownItem] = false;
        }
    }
}

// Handle close dropdown
function closeDropdown(dropDownName) {
    listDropDown.value[dropDownName] = false;
    // Handle emit event to components/Header.vue
    $emits('handle-modal', false);
}

</script>