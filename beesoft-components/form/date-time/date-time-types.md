---
description: These are the types used in the Date/Time component.
---

# Date/Time Types

`DateTimeSelectionType` is used to tell the component the type of selector to use.

```typescript
enum DateSelectionType {
  DateTime = 0,
  DateOnly = 1,
  TimeOnly = 2,
  DateRange = 3,
}
```

`DateFormatType` is used to determine how the date string is formatted.

```typescript
enum DateFormatType {
  Short,
  Medium,
  Long,
}
```

`TimeConstraints` is used to allow the time selector to increment by more than a single value. Only if a property is set will it be applied to the selector; for example setting the `minutes` property could allow the minutes to increase by five minutes instead of one.

```typescript
interface TimeConstraints {
  hours?: IncrementConstraint;
  minutes?: IncrementConstraint;
  seconds?: IncrementConstraint;
}
```

`IncrementConstraints` is used when a time selector needs to increment by more than just a single value. An example would be if you want the minutes to increment by five instead of one; you would need to set `min` to 0, `max` to 59, and `step` to 5.

```typescript
interface IncrementConstraint {
  min: number;
  max: number;
  step: number;
}
```

`CalendarIconPosition` allows the selection icon to be positioned to the left or the right.

```typescript
enum CalendarIconPosition {
  Right,
  Left,
  None,
}
```
