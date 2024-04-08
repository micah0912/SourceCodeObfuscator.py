# Source Code Formatter

🟆 [mSCF.py](https://github.com/micah0912/mSCF.py)

![Release](https://img.shields.io/github/v/release/micah0912/mSCL.py?style=flat-square&color=blue)
![Stability-Beta](https://img.shields.io/badge/stability-mature-blue.svg?style=flat-square)
[![Licence-GPLv3](https://img.shields.io/badge/license-GPLv3-blue.svg?style=flat-square)](https://github.com/micah0912/SCL.py/blob/master/LICENSE)
![Requirement-Paython-3.10](https://img.shields.io/badge/paython-%3E=3.10-blue.svg?style=flat-square)

- A powerfully source cdoe <u>**Format Manager**</u>.
- Developed for improved management of personal projects, and free to use.
- Spinoff from [mSCX.py](https://github.com/micah0912/mSCX.py).
- Built on [spairaru.py](https://github.com/etrotech/spairaru.py) framework.
- For collaboration or service requests, contact [@M](https://github.com/micah0912) ( English, 日本語, 中文 ).
- A coffee donation will help keep the package updated :)

<tab>
<br>

### Highlights
---

SCF has been designed with two distinct functionalities: **"Beautify"** and **"Minify"** for source code optimization.

**Beautify** :
- Formats elements for improved readability.
- Enhances code clarity by formatting comments.
- Removes extraneous lines, spaces, and tabs to streamline code structure.
- Modify Document Indentation, Linebreak Sequence, and Encoding.

**Minify** : 
- Enhances efficiency by removing comments.
- Seamlessly joins lines for maximum compactness.
- Minimizes file size by eliminating unnecessary lines, spaces, and tabs.
- Modify Document Linebreak Sequence and Encoding.

<tab>
<br>

### Languages
---

**Across Platform Application Language**
> .c, .h, .java, .js, .php, .py, .ts

**Console Application Language**
> .bash, .cmd, .sh, .zsh

**Informational Language**
> .cf, .cfg, .cnf, conf, .env, .ini, .json

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

##### A: PIP

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

#### 1: To beautify source code

<details>
<summary>long syntax</summary>
<br>

```python

from mSCF import SourceCodeFormatter

SourceCodeFormatter.beautify( "__path_of_application_root__" )


```

</details>

<details>
<summary>short syntax</summary>
<br>

```python

from mSCF import scf

scf.btfy( "__path_of_application_root__" )

```

</details>

<tab>
<br>

#### 2: To minify source code

<details>
<summary>long syntax</summary>
<br>

```python

from mSCF import SourceCodeFormatter

SourceCodeFormatter.minify( "__path_of_application_root__" )


```

</details>

<details>
<summary>short syntax</summary>
<br>

```python

from mSCF import scf

scf.mnfy( "__path_of_application_root__" )

```

</details>

<tab>
<br> 

### Advanced Usage
---

*Beautify Options*

`omit_line` :
- Omit all removable empty lines.
- Defaults to `true`.

`omit_space` :
- Omit between spaces.
- Remove all removable leading, trailing spaces.
- Defaults to `true`.

`omit_tab` :
- Omit between tabs.
- Remove all removable leading, trailing tabs.
- Defaults to `true`.

`format_comment` :
- Format all comments.
- Defaults to `true`.

`format_element` :
- Format all coding elements.
- Defaults to `true`.

`format_callable` :
- Formats class, method, function, or any callables.
- Requires `format_element` option to be enabled.
- Defaults to `true`.

`format_collection` :
- Formats array, dictionary, tuple or any collection type objects.
- Requires `format_element` option to be enabled.
- Defaults to `true`.

`format_variable` :
- Formats variable, constant, or any defines.
- Requires `format_element` option to be enabled.
- Defaults to `true`.

<br> 

*Minify Options*

`keep_structure` :
- When this is enabled, preserves the leading spaces or tabs of each line.
- Defaults to `false`.

`remove_line` :
- Remove all removable empty lines.
- Defaults to `true`.

`remove_space` :
- Remove all removable leading, between, trailing spaces.
- Defaults to `true`.

`remove_tab` :
- Remove all removable leading, between, trailing tabs.
- Defaults to `true`.

`remove_comment` :
- Remove all comments.
- Defaults to `true`.

`remove_multiple_line_comment` :
- Remove all multiple-line comments. 
- Requires `remove_comment` option to be enabled.
- Defaults to `true`.

`remove_single_line_comment` :
- Remove all single-line comments.
- Requires `remove_comment` option to be enabled.
- Defaults to `true`.

#### 1: Copy to Targeted Folder and Apply Licensing

By giving `distribution` option, **SCF** will create a copy of target files and write to the copies.

<details>
<summary>long syntax</summary>
<br>

```python

SourceCodeFormatter.license(
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

scf.lic(
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

When target file is a symbolic link, with `follow_link` option enabled, **SCF** will either write to source file. Default is `false`.

<details>
<summary>long syntax</summary>

```python

SourceCodeFormatter.license(
	"__path_of_application_root__" 
	# Search Options
	, follow_link = True
)

```

</details>

<details>
<summary>short syntax</summary>

```python

scf.lic(
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

### Custom - Filter
---

**SourceCodeCharacterFilter** : 
- Contains Filters used to manage programing characters.

**SourceCodeCleanupFilter** :
- Contains Filters used to control decision or result in cleanup process.

**SourceCodeLayoutFilter** :
- Contains Filters used to control decision or result in layout process.

<br>

*Example of Changing RemoveHead Descision*

\* when user enables the option `omit_space` or `omit_tab` or `remove_space` or `remove_tab`, RemoveHead filter will triggered to make further decisions based on the programming language.

<details>
<summary>long syntax</summary>
<br>

```python

from mSCF import SourceCodeCleanupFilter


SourceCodeFormatter.filter(
	# filter_name
	SourceCodeCleanupFilter.RemoveHead
	# filter_listener
	, (
		lambda
			sFilter__
			, decision__
			, file_extension_
		:
			return final_decision__
	)
)

```

</details>

<details>
<summary>short syntax</summary>
<br>

```python

from mSCF import ScClnupFltr


scf.fltr(
	# filter_name
	ScClnupFltr.RmHd
	# filter_listener
	, (
		lambda
			sFltr__
			, dcsn__
			, fl_ext__
		:
			return fin_dcsn__
	)
)

```

</details>

<br>

*Example of Modify Layout Result*

\* when user enables the option `format_element`, ElementFormatedContent filter will triggered to determine if further editing is necessary.

<details>
<summary>long syntax</summary>
<br>

```python

from mSCF import SourceCodeLayoutFilter


SourceCodeFormatter.filter(
	# filter_name
	SourceCodeLayoutFilter.ElementFormatedContent
	# filter_listener
	, (
		lambda
			sFilter__
			, orignal_content__
			, mTargetFile__
			, linebreak_symbol__
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

from mSCF import ScLyoFltr


scf.fltr(
	# filter_name
	ScLyoFltr.ElFmtdCnt
	# filter_listener
	, (
		lambda
			sFltr__
			, orig_cnt__
			, mTgtFl__
			, lnbrk_smbo__
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

🟆 [mSCL.py](https://github.com/micah0912/mSCL.py)
 - Source Code License Manager

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
