# use-oscillator

A simple react hook that produces an interface `OscillatorNode` with default settings.


```ts
import React from "react"
import useOscillator from "use-oscillator"

interface Props {
  updateFrequency: (f: number) => void
}
export default ({updateFrequency }: Props) => {
  const { start, stop } = useOscillator(frequency)
  return (
    <ul>
      <li>
        <button onClick={stop}>stop</button>
      </li>
      <li>
        <button onClick={start}>start</button>
      </li>
      <li>
        <input
          value={frequency}
          onChange={(e) => updateFrequency(Number(e.target.value))}
        ></input>
      </li>
    </ul>
  )
}

```
