####mastache
https://github.com/janl/mustache.js/
##Javascript Model engine mustache.js

quick example:
	var view = {
  		title: "Joe",
  		calc: function () {
    		return 2 + 4;
  		}
	};

	var output = Mustache.render("{{title}} spends {{calc}}", view);
In this example, the Mustache.render function takes two parameters
1. Mustache template
2. A view object that contains the data and code needed to render the template

Mustache.render(
  template            : String,
  view                : Object,
  partials?           : Object,
  tags = ['{{', '}}'] : Tags,
) => String

Mustache.parse(
  template              : String,
  tags = ['{{', '}}']   : Tags,
) => Token[]



{{xx}} 取变量名
{{{xxx}}}  {{$xxx}} 如果变量是html格式字符串, 保持原有格式
Section: 用作循环	
 {{#xxx}} 变量有内容才显示{{/xxxx}} 
 {{^xxx}} 变量没有内容才显示 {{/xxx}} 