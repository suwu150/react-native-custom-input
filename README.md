# react-native-custom-textInput
react-native-custom-input,一个自定义的输入组件    
The final rendering
----
![The final rendering](https://github.com/suwu150/react-native-custom-input/blob/master/react-native-custom-input.gif?raw=true)

Installation:  
-------------------------------------- 
```
 npm install --save react-native-custom-input
```
Example usage: 
--------------------------------------- 
1.basic     

```javascript
import Input from react-native-custom-input;

   ...
  render() {
    return (
        <Input />
    );
  }
```

Props:   
---------------------------------------

|Props|Explain|type|require|default|          
|:-------|:--------|:--------|:-------|:----------|
|label|输入框的名称|string|no|文本输入框|    
|value|输入框的值|any|yes|''|    
|labelTextStyle|输入框的名称的样式|string|no|{ width: 100,flexDirection: 'row',justifyContent: 'flex-end', alignItems: 'center',marginLeft: 15,}|     
|required|是否显示必输标志|boolean|no|false|   
|mode|输入框的模式，具体有简单输入框还是输入域|string|no|简单文本输入框，值为（'Input'，'TextArea'）两者之一|      
|textInputStyle|输入框的样式|object|no|{fontSize: 14, color: '#332f2b'}|  
|isUpdate|是否可编辑，true为可编辑|boolean|no|true|     
|suffix|输入框后面的后缀，值得注意的是length大于3的时候将不会显示|string|no|''|
|placeholderTextColor|占位符文字的颜色|string|no|'#ccc8c4'|     
|autoCapitalize|首字母是否自动大写|string|no|'none'，只能是['characters', 'words', 'sentences', 'none']之一|   
   
`注意： 由于输入框组件是在react-native官方组件的基础上进行封装，所以支持TextInput所有属性，在这里就不一一罗列`


Examples from props:
```javascript
...
  _onChange = (label, value) => {
    this.setState({ [label]: value });
  };

  render() {
    return (
      <View style={styles.container}>
        <Text>
          {this.state.result}
        </Text>
        <Input onChange={(value) => this._onChange('input1', value)} value={this.state.input1 || ''} />
        <Input label={'姓名'} onChange={(value) => this._onChange('input2', value)} value={this.state.input2 || ''} />
        <Input onChange={(value) => this._onChange('input3', value)} mode={'TextArea'} label={'详细地址'} value={this.state.input3 || ''} />
      </View>
    );
  }
...

```

LICENSE: 
-------   
MIT

