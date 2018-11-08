StarUML的Python扩展
这个StarUML（http://staruml.io）扩展支持从UML模型生成Python代码。从StarUML的Extension Manager安装此扩展。

Python代码生成
点击菜单（Tools > Python > Generate Code...）
选择将为Python生成的基本模型（或包）。
选择将放置生成的Python源文件（.py）的文件夹。
Belows是从UML模型元素转换为Python源代码的规则。

UMLPackage
转换为python 包（作为文件夹__init__.py）。
UMLClass，UMLInterface
转换为python 类定义作为分离的模块（.py）。
生成默认构造函数（def __init__(self):）
documentation 属性为docstring
UMLEnumeration
转换为从Enum继承的python类作为一个独立的模块（.py）。
文字转换为类变量
UMLAttribute，UMLAssociationEnd
转换的实例变量如果isStatic属性为true，或一个类变量，如果isStatic属性是假
name 属性到标识符
documentation 属性为docstring
如果multiplicity是一0..*，1..*，*，则变量将与初始化[]。
UMLOperation
转换为一个实例方法，如果isStatic属性为true，或一个类的方法（@classmethod）如果isStatic属性是假
name 属性到标识符
documentation 属性为docstring
UMLParameter到方法参数
UMLGeneralization，UMLInterfaceRealization
转换为继承

