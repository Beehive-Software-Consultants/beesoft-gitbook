---
description: These are the types used within the Overlay Panel
---

# Overlay Panel Types

`DomTargetPosition` is used by the overlay positioning code to determine which part of the target the overlay should connect to.

```typescript
enum DomTargetPosition {
  TopLeft = 0,
  TopRight = 1,
  BottomLeft = 2,
  BottomRight = 3,
}
```

`DomElementAlignment` is used by the overlay positioning code to determine which part of the overlay is used to connect to the target.

```typescript
enum DomElementAlignment {
  TopLeft = 0,
  TopRight = 1,
  BottomLeft = 2,
  BottomRight = 3,
}
```

`DomOffScreenLocation` is used by the `keep on screen` feature to tell the overlay which part is currently off screen (if any). If all are false then the overlay is fully on screen.

```typescript
interface DomOffScreenLocation {
  left: boolean;
  top: boolean;
  right: boolean;
  bottom: boolean;
}
```
