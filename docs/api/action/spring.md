---
title: Spring
description: An accurate, versatile spring animation.
category: action
---

# Spring

A spring animation based on `stiffness`, `damping` and `mass`.

This simulation offers smoother motion and a greater variety of spring-feels than the basic spring integration found in [physics](/api/physics).

It's based on the equations governing a [damped harmonic oscillator](https://en.wikipedia.org/wiki/Harmonic_oscillator#Damped_harmonic_oscillator), the same as those underlying Apple's `CASpringAnimation`.

`spring(props <Object>)`

## Props
- `stiffness <Number>`: The spring stiffness (default: `100`)
- `damping <Number>`: The strength of the friction force used to dampen motion (default: `10`)
- `mass <Number>`: Mass of the moving object. (default: `1.0`)
- `velocity <Number>`: The initial velocity of the spring. (default: `0.0`)
- `from <Number>`: Start from this number. (default `0`)
- `to <Number>`: End at this number. (default `0`)
- `restDisplacement <Number>`: End the animation if the distance to target is below this value (and `restSpeed`) (default: `0.01`)
- `restSpeed <Number>`: End the animation if the speed drops below this value (and `restDisplacement`) (default: `0.01`)

[...Action](/api/action)

## Methods

[...Action](/api/action)

## Playground

```javascript
import { spring } from 'popmotion';
```

```marksy
<Example template="Ball">{`
const ball = document.querySelector('.ball');
const ballRenderer = css(ball);

spring({
  mass: 2,
  stiffness: 1000,
  damping: 50,
  to: 300,
  onUpdate: (v) => ballRenderer.set('x', v)
}).start();
`}</Example>
```
