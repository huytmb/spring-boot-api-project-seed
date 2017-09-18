![Licence](https://img.shields.io/badge/licence-none-green.svg)
[![GitHub Release](https://img.shields.io/github/release/lihengming/spring-boot-api-project-seed.svg)](https://github.com/lihengming/spring-boot-api-project-seed/releases)
## Giới thiệu
Spring Boot API Project Seed dựa trên Spring Boot & MyBatis，phát triển nhanh chóng các dự án dựa trên RESTful API.

## Tính năng
- Cấu trúc project hợp lý, xây dựng theo Profiles, POM（[Cấu trúc Project](https://github.com/lihengming/java-codes/blob/master/shared-resources/github-images/project-struct.png)）
- Response thống nhất
- Xử lý Exception thống nhất
- Sử dụng Druid Spring Boot Starter
- Sử dụng FastJsonHttpMessageConverter
- Tích hợp MyBatis, Mapper, PageHelper, SQL
- Tự động tạo Model、Mapper、MapperXML、Service、ServiceImpl、Controller và một số class tiện ích khác.
 
## Quick Start
1. Fork project
2. Đến package ```test``` chứa ```CodeGenerator``` class.
3. Sử dụng ```demo-user.sql``` trong ```test resources```，để khởi tạo dữ liệu ban đầu.
3. Nhập tên table cần generator trong ```CodeGenerator.main()```
4. Run ```CodeGenerator.main()```
5. Cập nhật profile ```application-dev.properties```. Run Srping boot...have fun !
 
## Lưu ý khi phát triển
- Tên bảng: chữ thường, các chữ được sử dụng ký tự ```_``` để nối. Ví dụ: shift_work.
- Model ánh xạ tương ứng các trường dữ liệu trong table，đối với các thuộc tính mở rộng（ngay cả các thuộc tính nằm tại các table khác）đề xuất khởi tạo DTO，hoặc nếu bổ sung thuộc tính vào Model cần kèm theo Annotation ```@Transient```, chi tiết [Mapper](https://mapperhelper.github.io/docs/2.use/)
- Exception trong Service layer sử dụng throw ```ServiceException("message")```，thống nhất kiểu trả về Exception，ví dụ ```throw new ServiceException("Duplicate Username")```，response trả về ```{"code":400,"message":"Duplicate Username"}```，xử lý response trả về theo một quy chuẩn chung.
- Các thư viện utils chung ```apache-commons-*``` và ```guava```.
- Conventions cho JAVA của Alibaba（[Phiên bản mới nhất](https://github.com/lihengming/java-codes/blob/master/shared-resources/%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4Java%E5%BC%80%E5%8F%91%E6%89%8B%E5%86%8CV1.2.0.pdf))
- Đặc tả API:[ShowDoc](https://github.com/star7th/showdoc)、[SpringFox-Swagger2](https://github.com/springfox/springfox) 、[RAP](https://github.com/thx/RAP).
 
## Tài liệu
- Spring Boot（[Tổng quan Spring Boot](http://www.jianshu.com/p/1a9fd8936bd8)）
- MyBatis（[Tài liệu chính thức của China](http://www.mybatis.org/mybatis-3/zh/index.html)）
- MyBatis Mapper Plugin（[Documentation](https://mapperhelper.github.io/docs/)）
- MyBatis PageHelper Paging Plugin（[Documentation](https://pagehelper.github.io/)）
- Druid Spring Boot Starter（[Github](https://github.com/alibaba/druid/tree/master/druid-spring-boot-starter/)）
- Fastjson（[Wiki](https://github.com/Alibaba/fastjson/wiki/%E9%A6%96%E9%A1%B5)）
- ...

## License
Bấm [Star](https://github.com/lihengming/spring-boot-api-project-seed/stargazers) & [Fork](https://github.com/lihengming/spring-boot-api-project-seed/network/members)。
