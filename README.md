# PHP + Apache 

Chỉnh sửa Do It Yourself cartridge của Openshift. Cung cấp PHP 5.5+ và cấu hình Apache đầy đủ, có thể xem ở thư mục `conf`.

## Cài đặt nhanh

[![Cài đặt PHP OpenShift](http://launch-shifter.rhcloud.com/launch/Install PHP.svg)](https://openshift.redhat.com/app/console/application_type/custom?&cartridges[]=diy-0.1&initial_git_url=https://github.com/ladyga14/openshift-php.git&name=php)

1. Mở https://openshift.redhat.com/app/console/application_type/cart!diy-0.1
2. Điền vào **Source Code**: `https://github.com/ladyga14/openshift-php.git` và **Branch/Tag** phiên bản php bạn muốn sử dụng. Hiện tại hỗ trợ 3 phiên bản:
  * php5.5
  * php5.6
  * php7
3. Click **Create Application** và đợi
4. Mở website của bạn (vd: foo-bar.rhcloud.com ) và giữ cho trình duyệt mở. Trong thời gian đó bạn có thể `git clone` ứng dụng và bắt đầu code.
5. **IMPORTANT** : Trong khi ứng dụng đang build thì bạn không được `git push` trong thời gian đó.

### Tips

* Quá trình cài đặt sẽ diễn ra trong khoảng 20-30 phút.
* Mặc định nếu bạn không điền branch thì sẽ chọn phiên bản php5.6 để cài đặt
* Khi chỉnh sửa `conf/httpd.conf`, bạn phải load lại ứng dụng, hoặc chạy `${OPENSHIFT_REPO_DIR}/.openshift/action_hooks/reload` để nó hoạt động.
