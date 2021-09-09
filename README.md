# https://fullstackopen.com/en/part1/a_more_complex_state_debugging_react_apps

[object spread syntax](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)

Old version using one state object:
```
const App = () => {
  const [clicks, setClicks] = useState({
    left: 0, right: 0
  })

  const handleLeftClick = () =>
    setClicks({ ...clicks, left: clicks.left + 1 })

  const handleRightClick = () =>
    setClicks({ ...clicks, right: clicks.right + 1 })

  return (
    <div>
      {clicks.left}
      <button onClick={handleLeftClick}>left</button>
      <button onClick={handleRightClick}>right</button>
      {clicks.right}
    </div>
  )
}
```