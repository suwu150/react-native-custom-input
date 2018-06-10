# react-native-custom-textInput
react-native-custom-input,一个自定义的输入组件    
The final rendering
----
![The final rendering](https://github.com/suwu150/static-resource/blob/master/images/react-native-string-distion.gif?raw=true)

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
        <TextInput
        />
    );
  }
```

Props:   
---------------------------------------

|Props|Explain|type|require|default|          
|:-------|:--------|:--------|:-------|:----------|
||the string that needs to be split|string|yes|''|       
|delimiter|split string|string|no|no|     
|style|container style|object|no|{ alignItems: 'flex-end' }|     
|frontStyle|The style in the string before the split symbol|object|no|no|  
|delimiterStyle|Split symbol style|object|no|no|     
|behindStyle|The style behind the split symbol in the string|object|no|{}|     

Examples from props:
```javascript

```

LICENSE: 
-------   
MIT

