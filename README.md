
# react-native-selectable-text
## Usage
### Aşağıdaki kullanıma ek olara bazı proplar eklendi. 

- onSelectionPosition : Text seçimi sonrası seçilen context'i ve başlangıç bitiş noktalarını verir
- RenderActionBar : Seçim sonrası ekranda gösterilmesini istediğiniz komponent renderlanır.
- RenderActionBar property sini kullanırken menuItemsi kaldırın.

```javascript
import { SelectableText } from "@astrocoders/react-native-selectable-text";

// Use normally, it is a drop-in replacement for react-native/Text
<SelectableText
  menuItems={["Foo", "Bar"]}
  onSelectionPosition={{ content, selectionStart, selectionEnd }=>{}}
  RenderActionBar={()=><MyComponent>}
  onSelection={({ eventType, content, selectionStart, selectionEnd }) => {}}
  value="I crave star damage"
/>;
```


## Props
| name | description | type | default |
|--|--|--|--|
| **value** | text content | string | "" |
| **onSelection** | Called when the user taps in a item of the selection menu | ({ eventType: string, content: string, selectionStart: int, selectionEnd: int }) => void | () => {} |
| **menuItems** | context menu items | array(string) | [] |
| **style** | additional styles to be applied to text | Object | null |
| **highlights** | array of text ranges that should be highlighted with an optional id | array({ id: string, start: int, end: int }) | [] |
| **highlightColor** | highlight color |string | null |
| **onHighlightPress** | called when the user taps the highlight  |(id: string) => void | () => {} |
| **appendToChildren** | element to be added in the last line of text | ReactNode | null |
| **TextComponent** | Text component used to render `value` | ReactNode | <Text> |
| **textValueProp** | text value prop for TextComponent. Should be used when passing TextComponent. Defaults to 'children' which works for <Text> | string | 'children' |
| **textComponentProps** | additional props to pass to TextComponent | object | null |

