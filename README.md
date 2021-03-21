# JavascriptApp1
Javacriptのクラスを使ってみたよ


## 成果物
|![ed8c80f176ceebcabbd6d1663e49d91d](https://user-images.githubusercontent.com/45095615/111894942-6d432380-8a52-11eb-940e-473c69966aff.gif)|
|:--|


## コード
```js
'use strict';

{
  class Sum {
    constructor() {
    }

    calculate() {
      const p = document.createElement('p');
      const a = document.querySelector('#inputA');
      const b = document.querySelector('#inputB');
      const sum = document.querySelector('#sum');
      const valueA = Number(a.value);
      const valueB = Number(b.value);

      p.textContent = `合計：${valueA + valueB}`;

      while (sum.firstChild) {
        sum.removeChild(sum.firstChild);
      }
      sum.appendChild(p);
    }
  }
  const sum = new Sum();
  sum.calculate();

  const inputs = document.querySelectorAll('input')
  inputs.forEach((input) => {
    input.addEventListener('input', () => {
      sum.calculate();
    })
  })
}
```


