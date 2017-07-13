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
2. Đến package ```test``` thực thi ```CodeGenerator```
3. 如果只是想根据上面的演示来亲自试试的话可以使用```test resources```目录下的```demo-user.sql```，否则忽略该步
3. 输入表名，运行```CodeGenerator.main()```方法，生成基础代码（可能需要刷新项目目录才会出来）
4. 根据业务在基础代码上进行扩展
5. 对开发环境配置文件```application-dev.properties```进行配置，启动项目，Have Fun！
 
## Lưu ý khi phát triển
- 表名，建议使用小写，多个单词使用下划线拼接
- Model内成员变量建议与表字段数量对应，如需扩展成员变量（比如连表查询）建议创建DTO，否则需在扩展的成员变量上加```@Transient```注解，详情见[通用Mapper插件文档说明](https://mapperhelper.github.io/docs/2.use/)
- 建议业务失败直接使用```ServiceException("message")```抛出，由统一异常处理器来封装业务失败的响应结果，比如```throw new ServiceException("该手机号已被注册")```，会直接被封装为```{"code":400,"message":"该手机号已被注册"}```返回，无需自己处理，尽情抛出
- 需要工具类的话建议先从```apache-commons-*```和```guava```中找，实在没有再造轮子或引入类库，尽量精简项目
- 开发规范建议遵循阿里巴巴Java开发手册（[最新版下载](https://github.com/lihengming/java-codes/blob/master/shared-resources/%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4Java%E5%BC%80%E5%8F%91%E6%89%8B%E5%86%8CV1.2.0.pdf))
- 建议在公司内部使用[ShowDoc](https://github.com/star7th/showdoc)、[SpringFox-Swagger2](https://github.com/springfox/springfox) 、[RAP](https://github.com/thx/RAP)等开源项目来编写、管理API文档
 
## Tài liệu
- Spring Boot（[Tổng quan Spring Boot](http://www.jianshu.com/p/1a9fd8936bd8)）
- MyBatis（[Tài liệu chính thức của China](http://www.mybatis.org/mybatis-3/zh/index.html)）
- MyBatis Mapper Plugin（[查看官方中文文档](https://mapperhelper.github.io/docs/)）
- MyBatis PageHelper Paging Plugin（[查看官方中文文档](https://pagehelper.github.io/)）
- Druid Spring Boot Starter（[查看官方中文文档](https://github.com/alibaba/druid/tree/master/druid-spring-boot-starter/)）
- Fastjson（[查看官方中文文档](https://github.com/Alibaba/fastjson/wiki/%E9%A6%96%E9%A1%B5)）
- ...

## License
Bấm [Star](https://github.com/lihengming/spring-boot-api-project-seed/stargazers) & và [Fork](https://github.com/lihengming/spring-boot-api-project-seed/network/members)。
