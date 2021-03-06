---
# __PFSENSE BUILD GUIDE__

---

# Setup build environment
- Create build machine (FreeBSD VM) from https://download.freebsd.org/ftp/releases/amd64/amd64/ISO-IMAGES/12.1/FreeBSD-12.1-RELEASE-amd64-dvd1.iso 

- Khi thực hiện cài đặt, lưu ý chọn Partioning là Auto ZFS

- Sửa lại build tools để build từ local source code thay vì check out từ git:
Trong file tools/builder_common.sh line 1746 sửa ```-m git -U ${FREEBSD_REPO_BASE_POUDRIERE}``` thành ```-m src=/root/FreeBSD-src-RELENG_2_5```

# Build ISO from source code
- Setup jail (FreeBSD jail là một tool cho phép tạo virtual environment với các source kernel khác nhau trên cùng một build machine): ```./build.sh --setup-poudriere```

- Build FreeBSD Port (Để quản lý và cài đặt các package trong FreeBSD): ```./build.sh --update-pkg-repo```

- Build Kernel and create ISO: ```./build.sh --skip-final-rsync iso```


# Install pfense from ISO 
Sau khi đã build thành công file ISO, có thể sử dụng file ISO này để cài đặt pfsense tương tự như một file ISO thông thường của FreeBSD