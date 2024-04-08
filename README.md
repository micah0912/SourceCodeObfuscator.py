# [Source Code Licenser](http://www.micah-t.xyz)

aka mSCL.py

![Release](https://img.shields.io/github/v/release/micah0912/mSCL.py?style=flat-square&color=blue)
![Stability-Beta](https://img.shields.io/badge/stability-mature-blue.svg?style=flat-square)
[![Licence-GPLv3](https://img.shields.io/badge/license-GPLv3-blue.svg?style=flat-square)](https://github.com/micah0912/SCL.py/blob/master/LICENSE)
![Requirement-Paython-3.10](https://img.shields.io/badge/paython-%3E=3.10-blue.svg?style=flat-square)

- A powerfully source cdoe <u>**License Manager**</u>.
- Developed for improved management of personal projects, and free to use.
- Spinoff from [mSCX.py](https://github.com/micah0912/mSCX.py).
- Built on [spairaru.py](https://github.com/etrotech/spairaru.py) framework.
- For collaboration or service requests, contact [@M](https://github.com/micah0912) ( English, 日本語, 中文 ).
- A coffee donation will help keep the package updated :)

<tab>
<br>

### Highlights
---

Follow your scenario with no limit on development or release branches, or development or production states. **SCL** empowers you to:
- easily License or Unlicense files, toggle accordingly.
- add or remove license texts 
	- to all or specified file;
	- using default or customized templates.
- Automatically generate a LICENSE.txt file with default or customized templates.

<tab>
<br>

### Languages
---

**Across Platform Application Language**
> .c, .h, .java, .js, .php, .py, .ts

**Console Application Language**
> .bash, .cmd, .sh, .zsh

**Informational Language**
> .cf, .cfg, .cnf, conf, .env, .ini

**Native Application Language** 
> .swift

**Web Application Language** 
> .css, .html, .sass, .xml


<tab>
<br>

### Requirements
---

1. [Python](https://www.python.org) version 3.10+

<tab>
<br>

### Dependencies
---

1. [spairaru.py](https://github.com/etrotech/spairaru.py) version 1.0+

<tab>
<br>

### Installation
---

#### A: PIP

```python

* coming soon.

```

<tab>
<br>

#### B: Installer
1. Download from [Git](https://github.com/micah0912/mSCLmicah0912) or [Web](http://www.micah.xyz).
2. Extra and find installer in <u>\_\_installers\_\_</u> folder.
3. Execute installer according to you OS.

<tab>
<br>

#### C: Manually
1. Download from [Git](https://github.com/micah0912/mSCLmicah0912) or [Web](http://www.micah.xyz).
2. Extra and move **SCL** from <u>src</u> source or <u>dist</u> distribution folder, to <u>python path</u> or <u>working directory</u>.
3. Default path is set to 
	- *macOS* : 
		- */Library/Developer/CommandLineTools/Library/Frameworks/Python3.framework/Versions/{ version }/lib/python{ version }/site-packages/mSCL*
	- *Linux* : 
		- */usr/local/lib/python{ version }/dist-packages/mSCL*
	- *Windows* :
		- *\Program Files\Python{ version }\Lib\site-packages\mSCL*

<tab>
<br> 

### Basic Usage
---
### 1: To apply license

<details>
<summary>long syntax</summary>
<br>

```python

from mSCL import SourceCodeLicenser

SourceCodeLicenser.license( "__path_of_application_root__" )

```

</details>

<details>
<summary>short syntax</summary>
<br>

```python

from mSCL import scl

scl.lic( "__path_of_application_root__" )

```

</details>

<tab>
<br>

#### 2: To dispose license

<details>
<summary>long syntax</summary>
<br>

```python

from mSCL import SourceCodeLicenser

SourceCodeLicenser.unlicense( "__path_of_application_root__" )

```

</details>

<details>
<summary>short syntax</summary>
<br>

```python

from mSCL import scl

scl.ulic( "__path_of_application_root__" )

```

</details>

<tab>
<br> 

### Advanced Usage
---

*License Options*

`make_license_text_file` :
- Create LICENSE.txt if it does not exists in the root directory.
- Defaults to `false`.

`optional_divider` :
- Specifies the additional number of lines to be created after the License Template.
- Defaults is `0`.

<br> 

*Unlicense Options*

`optional_divider` :
- Specifies the additional number of lines to be created after the License Template.
- Defaults is `0`.

`remove_license_text_file` :
- Remove LICENSE.txt if it exists in the root directory.
- Defaults to `false`.

<br> 

#### 1: Copy to Targeted Folder and Apply Licensing

By giving `distribution` option, **SCL** will create a copy of target files and write to the copies.

<details>
<summary>long syntax</summary>
<br>

```python

SourceCodeLicenser.license(
	"__path_of_application_root__" 
	# Locational Options
	, distribution_directory = "__path_of_distribution_directory__" 
)

```

</details>

<details>
<summary>short syntax</summary>
<br>

```python

scl.lic(
	"__path_of_application_root__" 
	# Locational Options
	# distribution_directory
	, dist_dir = "__path_of_distribution_directory__" 
)

```

</details>

<tab>
<br>

#### 2: Process over Symbolic Folders and Files

When target file is a symbolic link, with `follow_link` option enabled, **SCL** will either write to source file. Default is `false`.

<details>
<summary>long syntax</summary>
<br>

```python

SourceCodeLicenser.license(
	"__path_of_application_root__" 
	# Search Options
	, follow_link = True
)

```

</details>

<details>
<summary>short syntax</summary>
<br>

```python

scl.lic(
	"__path_of_application_root__" 
	# Search Options
	# follow_link
	, flw_lnk = True
)

```

</details>

<br> 

For more options, advantaged examples, refer to [mSCF.py](http://www.micah-t.xyz)

<tab>
<br> 

### Customization
---
- Customization setting can be created by by storing custom files follow [mSCX.py](https://github.com/micah0912/mSCX.py) specification.
- In addition to the **.scx** folder, you can also place custom files in the **.scl** or **.scl.py** folders.

<tab>
<br>

### Custom - Template
---

- **.tpl**, the Template file provides the licensing text will be written into target file during licensing process.

*Example Hierarchy*

```

🏠
├─ 🖿 .scl
│  ├─ 🖺 xxx.apv
│  ├─ 🖺 xxx.env
│  ├─ 🖺 xxx.cnf
│  ├─ 🖺 xxx.ign
│  ├─ 🖺 xxx.ini
│  ├─ 🖺 xxx.tpl 👈
│  └─ ...
└─ ...

```

<tab>
<br>

#### Naming

- For default template, 
	1. name it as **@.tpl**;
	2. or name it in glob pattern ***.tpl**.
- To specify template, 
	1. name it as exactly the same as the target file;
	2. or name it in glob pattern, like **abc*.tpl**.

*Example of Naming*

```

🏠
├─ 🖿 .scl
│  ├─ 🖺 template.cnf 👈
│  ├─ 🖺 abc*.html.tpl 👈
│  └─ ...
├─ 🖺 abcd.html 👈
└─ ...

```
In the above hierarchy, the template **abc*.html.tpl** will apply to all html files start with **abc**. For all the other files, the template **@.tpl** will be applied.

<tab>
<br>

#### Design

- To include dynamic text in a template file, enclose variable with <u>double curly braces</u> along with <u>parentage mark</u>.
- Variables can be defined in **.cnf** configuration files.

*abc\*.html.tpl*

```

{{%SCL_PTN_NM}} {{%SCL_PTN_VER}}

Copyright {{%SCL_LIC_HLDR}} {{%SCL_LIC_YR}}. All Rights Reserved.

This file is part of {{%SCL_PTN_NM}}, which released under {{%SCL_LIC_TYP}}.

```
*template.cnf*

```

SCL_PTN_NM = mSCL.py
SCL_PTN_VER = sr1.0.0
SCL_LIC_HLDR = M
SCL_LIC_YR = 2022
SCL_LIC_TYP = GPL-3.0-or-later

```

*with variable placeholder converted, template outputs below*

```

mSCL.py sr1.0.0

Copyright M, and its contributor 2022. All Rights Reserved.

This file is part of mSCL.py, which released under GPL-3.0-or-later.

```

<tab>  
<br>

### Custom - Filter
---

**SourceCodeCharacterFilter** : 
- Contains Filters used to manage programing characters.

**SourceCodeLicenseFilter** :
- Contains Filters used to control decision or result in licensing process.

<br>

*Example of Editing A Commented Out Template*

<details>
<summary>long syntax</summary>
<br>

```python

from mSCL import SourceCodeLicenseFilter


SourceCodeFormatter.filter(
	# filter_name
	SourceCodeLicenseFilter.CommentedOutContent
	# filter_listener
	, (
		lambda
			sFilter__
			, orignal_content__
			, mTargetFile__
		:
			return final_content__
	)
)

```

</details>

<details>
<summary>short syntax</summary>
<br>

```python

from mSCF import ScLicFltr


scf.fltr(
	# filter_name
	ScLicFltr.CmtdoCnt
	# filter_listener
	, (
		lambda
			sFltr__
			, orig_cnt__
			, mTgtFl__
		:
			return fin_cnt__
	)
)

```

</details>

<tab>
<br>

### Dependent Projects
---

🟆 [mSCX.py](https://github.com/micah0912/mSCX.py)
- Source Code X

<tab>
<br>

### Peer Projects
---

🟆 [mSCF.py](https://github.com/micah0912/mSCF.py)
- Source Code Format Manager

🟆 [mSCO.py](https://github.com/micah0912/mSCO.py)
- Source Code Obfuscation Manager

<tab>
<br>

### ☕
---

If you feel this app useful and helpful, please support me to make it better.

<p style="float: left;">
	<a href="https://paypal.me/micaht0912" target="_blank"><img src="https://raw.githubusercontent.com/micah0912/M/master/__readme__/ast/m-paypal.jpg" alt="Paypal" style="width: 24%; "></a>
	<a href="" target="_blank"><img src="https://raw.githubusercontent.com/micah0912/M/master/__readme__/ast/m-alipay.jpg" alt="Alipay" style=" width: 24%;"></a>
	<a href="" target="_blank"><img src="https://raw.githubusercontent.com/micah0912/M/master/__readme__/ast/m-wechat.jpg" alt="Wechat" style="width: 24%;"></a>
</p>

<br>
