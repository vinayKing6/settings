#problems about post request attached to @PostMapping("<post path>"):
    the html file which implement post request must be put in templates/ directory otherwise it won't work

#problems abount jdbc in spring-boot:
    the version of jdbc driver used for connecting the sql must be equal to the version of sql
    for example: mysql v8 use jdbc driver v8.0.18

#problems about cookie:
    cookie value can not include <space> 

#static files should be put into target directory if changed  static files need be detected

#problems about jpa :
    @Column注解使用驼峰命名法时，会自动转换成下划线，例如userName=====user_name,所以数据表中字段名必须是下划线命名法
