# 自定义类型扩展

主要目的是为已有类型添加方法

编写java代码如下：
```java
import org.ssssssss.script.annotation.Comment;
/**
 * String类型转换
 */
@Component  //注入到Spring容器中，之后会被自动注册
public class StringFunctionExtension implements ExtensionMethod{
    @Override
	public Class<?> support() {
		return String.class;    //为String类型扩展方法
	}
    /**
	*	方法必须是public static 修饰,参数至少有一个,且第一个参数必须为support方法返回的类型
	*	以将字符串转为int为例,该方法编写如下,最终调用时使用strVar.toInt()调用
	*	该方法第一个参数会自动被传入,所以调用时无需传入
	*/
    @Comment("将字符串转为Integer(方法名的提示)")
	public static Integer toInt(String str){    // 第一个参数无需使用@Comment注解
		return NumberUtils.toInt(str);
	}


}
```
脚本中使用：
```js
var str = '123';
//以下两种方式都支持
return '1234'.toInt();
//return str.toInt();
```