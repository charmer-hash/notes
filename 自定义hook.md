自定义hook:

自定义hook函数，实现获取滚动距离Y

```javascript
import { useState} from 'react'

 function useWindowScroll(){
    const [y,setScrollY] = useState(0);
    window.addEventListener('scroll',() => {
        let scrollTop = document.documentElement.scrollTop;
        setScrollY(scrollTop);
    })
    return [y]
}
export {useWindowScroll};
```

