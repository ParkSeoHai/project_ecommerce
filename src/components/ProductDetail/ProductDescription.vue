<template>
    <div class="bg-color-white">
        <div class="product-desc-tab">
            <div class="product-desc-tab__title">
                Mô tả sản phẩm
            </div>
            
            <div
                class="product-desc-tab__content"
                :class="showViewAll ? 'show' : ''"
            >
                <p>
                    Đây là mô tả demo dành cho tất cả sản phẩm tại riêng website
                    https://wd-smart.myharavan.com/ không áp dụng cho theme khách hàng sử dụng
                </p>
                <h2>Điện thoại iPhone 12 Pro Max giá rẻ tại WD Smart</h2>
                <p>
                    Như cái tên gọi thì chắc hẳn các bạn cũng biết được <b>iPhone 12 Pro Max</b> chính là mẫu iPhone
                    12 đắt giá nhất cũng như cao cấp nhất của Apple. Điều này đồng nghĩa với việc chiếc máy
                    này sẽ sở hữu màn hình lớn nhất, công nghệ đỉnh cao nhất, hiện đại nhất mà <b>Apple</b> có thể
                    đưa ra.
                </p>
                <p>
                    <img src="https://file.hstatic.net/1000379792/file/camera-iphone-12-pro-max-chinh-hang-hai-phong_cb2be3e8d6da424d8ae6acda15452bb3.jpg"
                        alt="">
                </p>
                <h2>Cấu hình chi tiết iPhone 12 Pro Max Hải Phòng</h2>
                <p>
                    Trong số những mẫu <b>iPhone 12</b> đã lộ diện thì <b>iPhone 12 Pro Max</b> là mẫu có kích thước lớn
                    nhất lên tới 6.7
                    inches, thậm chí mẫu kế nhiệm là iPhone 11 Pro Max cũng nhỏ hơn một chút là 6.5 inches
                </p>
                <p>
                    <img src="https://file.hstatic.net/1000379792/file/cau-hinh-chi-tiet-iphone-12-pro-max_bcdca4f7a8ce42b889945868bd7fb011_grande.jpg"
                        alt="">
                </p>
                <h2>Cấu hình của iPhone 12 và iPhone 12 Pro</h2>
                <p>
                    Dù có kích thước lớn là vậy nhưng trang Mac Otakara của Nhật cho biết iPhone 12 Pro Max sẽ có độ dày
                    7.4mm, bằng với iPhone 12 Pro nhỏ hơn và mỏng hơn khá nhiều so với iPhone 11 Pro Max dày 8.1 mm. 
                </p>
                <h2>Thiết kế cụm bốn camera trên chiếc iPhone 12 Pro Max</h2>
                <p>
                    Có thể bạn không để ý nhưng những mẫu iPad Pro vài năm gần đây đã chuyển sang thiết kế cạnh phẳng giống
                    như iPhone 4 và iPhone 5 thời xưa, và đây cũng chính là ngôn ngữ thiết kế sẽ áp dụng cho iPhone 12 Pro
                    Max sắp tới.
                </p>
                <h2>Dung lượng bộ nhớ trong iPhone 12 Pro Max</h2>
                <p>
                    Vì là mẫu cao cấp và không còn quá nhiều phụ kiện đi kèm, nên bộ nhớ lưu trữ có thể là tính năng mà 
                    Apple sẽ bù đắp lại cho người dùng. Dự kiến 128GB sẽ là mức bộ nhớ trong tiêu chuẩn cho iPhone 12 
                    Pro Max và cao nhất là 512GB.
                </p>
                <p>
                    Ngoài việc cấu hình được nâng cấp thì thì camera cũng vậy, dự kiến iPhone 12 Pro Max sẽ có tới bốn 
                    camera ở mặt sau, hoặc vẫn là 3 camera nhưng thêm một cảm biến LiDAR giống như iPad Pro 2020.
                </p>
                <p>
                    <img src="https://file.hstatic.net/1000379792/file/iphone-12-pro-max-5g-hai-phong_a7908ea77b1145bc94b15bb7c4776a13.jpg" alt="">
                </p>
                <p>
                    Về máy quét LiDAR, chức năng chính của nó là sử dụng ánh sáng phản xạ để đo khoảng cách từ cảm biến 
                    đến các vật thể xung quanh cách xa tới 5 mét, thậm chí là có thể lập bản đồ môi trường xung quanh bạn 
                    ở cấp photon với tốc độ nano giây. Nhìn chung là sẽ hữu ích cho các tác vụ AR về lâu về dài.
                </p>
                <p>
                    Ngoài màn hình thì LG cũng sẽ là đối tác cung cấp mô-đun camera cho iPhone 12 Pro Max (cao cấp), 
                    hai đối tác khác là Sharp và O-film cung cấp cho hai mẫu cấp thấp còn lại.
                </p>
                <p>
                    <img src="https://file.hstatic.net/1000379792/file/tra-gop-iphone-12-pro-max-0_-tai-hai-phong_e2dfb737a586472bb55ed5a096492f49.jpg" alt="">
                </p>
                <p>
                    LG, Sharp và O-film sẽ chia sẻ đơn đặt hàng cho iPhone 12 máy ảnh. LG sẽ sản xuất mô-đun máy ảnh cho 
                    iPhone cao cấp hơn, trong khi Sharp và O-film sẽ sản xuất mô-đun máy ảnh cho iPhone cấp thấp hơn.
                </p>
            </div>

            <div class="view-all-tab">
                <button
                    class="view-all-tab__btn"
                    @click.prevent="showViewAll = !showViewAll"
                >
                    <i
                        class="bi view-all-tab__btn--icon"
                        :class="showViewAll ? 'bi-dash-circle' : 'bi-plus-circle'"
                    ></i>
                    {{ showViewAll ? 'Rút gọn' : 'Xem thêm' }}
                </button>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from "vue";

let showViewAll = ref(false);
</script>