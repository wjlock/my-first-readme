# my-first-readme
Repo explaining README.md


## Steps to Install on local computer
1. Go to [repo](https://github.com/SEI-ATL/tic-tac-toe) on Github profile
2. `fork` and `clone` repo
3. Clone to local machine
```text
git clone https://github.com/wjlock/my-first-readme.git
```
4. Go to `tic-tac-toe` directory
5. Open `index.html` in browser
```text
open index.html
```

```javascript
const handlePlayerClick = (e) => {
    console.log(e.target.classList)
    const cellValue = e.target.classList[1];
    
    const classList = e.target.classList;
    const location = classList[1]
    if (classList[2] === 'x' || classList[2] === 'o') {
        return;
    }



    if (xIsNext === true) {
        e.target.classList.add('x');
        verifyGameStatus();
    } else {
        e.target.classList.add('o');
        verifyGameStatus();
    }
}

resetButton.addEventListener('click', handleReset);

for (const cellDiv of cellDivs) {
    cellDiv.addEventListener('click', handlePlayerClick)
}
```

```css

.grid {
    background-color: salmon;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(3, 1fr);
    gap: 15px;
    margin-top: 50px;
}
```

```html
<div class="grid">
    <div class="box" id="box-1"></div>
    <div class="box" id="box-2"></div>
    <div class="box" id="box-3"></div>
    <div class="box" id="box-4"></div>
    <div class="box" id="box-5"></div>
    <div class="box" id="box-6"></div>
    <div class="box" id="box-7"></div>
    <div class="box" id="box-8"></div>
    <div class="box" id="box-9"></div>
    </div>
```

| Functions | Description |
| ----------- | ----------- |
| `handlePlayerClick` | Handle every single click|
| `verifyGameStatus` | Check the status after each turn |

## Usage
This game allows users to play Tic Tac Toe. Turns alternate between X and O, and win conditionas are checked on each click. The current turn and winner are both displayed at the bottom left.