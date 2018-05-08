# HtmlTest

# form表单
## form表单的作用
用于手机用户提交的信息。

## <form>标签 
<form>标签有4个属性
####  action
 定义在提交表单时执行的动作，后面跟上表单提交的地址
\  <form action="/lll" methord="post"> \
####  method
规定在提交表单时所用的 HTTP 方法,即定义表单提交的方式，有两种方式post 和 get
1.*get*
-  为提交的默认形式，使用 GET 时，表单数据在页面地址栏中是可见的，本质上是一个URL的拼接，即URL会把用户输入的信息组合起来（所有input中name属性的内容），这种方式不安全，且当提交数据多时，浏览器会被设定的容量限制。
- 适用情况：安全性要求不高的情况（没有敏感信息）；少量数据的提交；向后台要数据。
2. post
- URL不改变，即页面地址栏中被提交的数据是**不可见**的，安全性高。
- 适用情况：如果表单正在更新数据，或者包含敏感信息（例如密码）；向后台传数据。
#### target
在何处打开action,规定 action 属性中地址的目标
#### enctype
规定被提交数据的编码（默认：url-encoded）,当提交为文本形式时用text/plain;提交为多媒体时用multipart/form-data
***
## <input>标签 
input标签有个非常重要的属性type，根据属性值的不同，可以实现不同形式的输入。
代码形式：
<input  type="属性值" name="  " > 
#### text
- 文本输入，单行输入，不能换行，可在value中设置初始值。
- 代码示例：
 ` <input id="username" type="text" name="username" value="用户名"> `
#### password
- 用于密码输入，输入的内容显示为 圆点
-代码示例：
`<input id="password" type="password" name="password" > `
`<input id="password" type="password" name="password"  placeholder="输入密码"> `
 placeholder="输入密码"的作用是在输入框中提示输入密码。
#### checkbox
- 复选框，在**同**一个分组中，**name**属性的值是**一样**的，**value**值设置**不同**，这样浏览器就可以区分用户选了哪几项内容。
- 代码示例：
` <input type="checkbox" name="hobby" value="dota" >dota  `   
 ` <input type="checkbox" name="hobby" value="旅游" >旅游`
   `<input type="checkbox" name="hobby" value="宠物" >宠物` 

#### radio
- 单选框，使用方法和checkbox一样，区别是同一个分组只能选中一个
- 代码示例： 
` <input type="radio" name="sex2" value="男" >男 `
          `  <input type="radio" name="sex2" value="女" >女`
#### file
- 上传一个文件，可以限定上传文件的类型（但不靠谱，后台又要做这种限制）。
- 代码示例
`<input type="file" accept="image/gif,image/jpeg"/>`
#### hidden
- 用于暂存信息，在页面上显示不出来，但是内容会传递给后台。
  用处： 安全性考虑，后台可以检验这个数据，来保证输入时的环境是安全的，以防止别人伪造而修改数据库。
- - 代码示例
`<input type="hidden" name="abc" value="123"/>`
传递给后台的就是 abc=123

#### button
- 按钮，注意与<button>的区别，不提交内容。
- 代码示例
`<input type="button" name="button"/>`
#### reset
- 清空勾选的。
- 代码示例
`<input type="reset" name="reset"/>`
#### submit
- 提交
- 代码示例
`<input type="submit" name="submit"/>`
***
## 其他标签
####  Label
- 显示文本的标签，有个重要的属性for，for后面的值为某个标签的ID,当点击此label时，这个id的标签会被选中。
- 代码示例
` <label for="username">姓名</label>`
` <input id="username" type="text" name="username" value="用户名"> `
这时，当用鼠标点击【姓名】时，这个id为"username"的输入框就会被选中。
#### select
- 下拉菜单，每个选项的内容由<option>标签包裹。当某个<option>被设置为selected时，则该项为默认的初始值。
- 代码示例
`<select name="car" id="mycar">`
              `     <option value="兰博基尼">兰博基尼</option>`
              `     <option value="萨博"selected>萨博</option>`
                `  <option value="保时捷">保时捷</option>`
        `       </select>`
上面的萨博就是默认的选项。
