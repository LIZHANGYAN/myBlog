---
title: '[原]C#连接SQLServer'
tags:
  - SQL
  - C#
categories: 我怎么会这些杂七杂八的东西
date: 2014-04-19 00:07:16
---

首先你的头文件里必须引用
<!-- more -->

```
using System.Data;
using System.Data.SqlClient;
```
然后是连接数据库
```
SqlConnection con = new SqlConnection(Data Source=LZY; Initial Catalog=Student; Integrated Security=true)
```
其中Data Source后面给的是服务器名，我用的是本地数据库

Initial Catalog后面是数据库名；

Integrated Secutity后面如果为“true”或者“SSPI”，表示指定windows 身份验证，如果为“false”，表示不指定Windows身份验证；

然后是打开数据库
```
con.Open();
MessageBox.Show(数据库 + con.ServerVersion + con.State)
```
ServerVersion好像是可以看你数据库的下图蓝色圈里的数字，不知道是什么东西，State则是数据库的状态：打开还是关闭

![](http://img.blog.csdn.net/20140419000525593?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvdTAxMjYxMDI3Ng==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

附上一个完整代码

```

using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;
using System.Data.SqlClient;

namespace SQL
{
    public partial class OpenSQL : Form
    {
        public OpenSQL()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {

        }

        private void button1_Click(object sender, EventArgs e)
        {

            using (SqlConnection con = new SqlConnection(Data Source=LZY; Initial Catalog=Student; Integrated Security=true))
            {
                try
                {
                    con.Open();
                    MessageBox.Show(数据库+con.ServerVersion+con.State);</pre><pre code_snippet_id="300627" snippet_file_name="blog_20140419_5_992152"  class="csharp" name="code">                }
                catch (Exception ex)
                {
                    MessageBox.Show(ex.ToString());
                }
                finally
                {
                      con.Close();
                      MessageBox.Show(数据库+ con.State);
                      Application.Exit();
                }
            }
        }
    }
}

```
