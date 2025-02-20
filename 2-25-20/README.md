---
layout:
  title:
    visible: false
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: false
  pagination:
    visible: true
---

# 2-25-20

{% code overflow="wrap" fullWidth="true" %}
```toml
02-20-25
[react]
types = {
  DOM_Events: {
    [[React]]: [
      'each item listed below has its default (web) interface, a native type extension, and an EventHandler',
      [
        'UIEvent', 'DragEvent', 'FormEvent', 'FocusEvent', 
        'TouchEvent', 'InvalidEvent', 'AnimationEvent', 'ClipboardEvent', 
        'TransitionEvent','CompositionEvent', 'MouseEvent', 'WheelEvent', 
        'ChangeEvent', 'PointerEvent', 'KeyboardEvent'
      ],
      '.SyntheticEvent is a base type for all events - only use for (e) not included in the above list',
      @links [ReactTypes]:*Event:*Handler:Native* 
    ]
  }
  children: { 
    [[_]]: {
      "Remarks": [
        'cannot use type system to describe that the children are a certain type of JSX element',
        'ex. cannot describe a component which only accepts <ListItem> children'
      ]
    }
    [[React.ReactNode]]: [
      'broad definition of { children }',
      'it is a union type of all possible types that can be passed as chlidren in JSX',
      @links [ReactTypes]:ReactNode 
    ],
    [[React.ReactElement]]: [
      'more specific - only encompasses JSX Elements',
      'does NOT include JavaScript primitives (e.g. strings or numbers)',
      @links [ReactTypes]:ReactElement
    ]
  },
  style_props: {
    [[_]]: {
      "Remarks - Using bare React style API": [
        'uses React.CSSProperties - likely will not be used a lot, if at all',
        'i want to try and stick to pure tamagui style API if possible',
        'tamagui is built on RN props which are built on these props when transpiled so still good to know'  
      ],
    },
    [[Tamagui]]: [
      [
        'supports a superset of the ReactNative props, most notably RN ViewProps and StyleProps',
        'style props are added directly onto the same object',
        @links [RNViewProps, RNTextProps]
      ],
      [
        'non-style props added by tamagui are listed below',
        [
          'animation', 'animateOnly', 'theme', 'themeInverse', 'themeShallow', 'forceStyle', 
          'hitSlop', 'group', 'componentName', 'className', 'disableClassName', 'tag', 
          'debug', 'untilMeasured', 'disableOptimization', 'tabIndex', 'role', 'asChild'
        ],
        @links [TamaguiProps]
      ],
    ],
  } 
} #
```
{% endcode %}
