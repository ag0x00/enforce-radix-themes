# Radix Themes API Reference

Quick reference for `@radix-ui/themes` components and props.

## Layout Components

### Flex

```tsx
import { Flex } from '@radix-ui/themes';

<Flex
  direction="row" | "column" | "row-reverse" | "column-reverse"
  align="start" | "center" | "end" | "baseline" | "stretch"
  justify="start" | "center" | "end" | "between"
  wrap="nowrap" | "wrap" | "wrap-reverse"
  gap="1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"
  gapX="1"-"9"
  gapY="1"-"9"
  // Shared layout props below
>
```

### Grid

```tsx
import { Grid } from '@radix-ui/themes';

<Grid
  columns="1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9" | string
  rows="repeat(2, 64px)" | string
  flow="row" | "column" | "dense" | "row-dense" | "column-dense"
  align="start" | "center" | "end" | "baseline" | "stretch"
  justify="start" | "center" | "end" | "between"
  gap="1"-"9"
  gapX="1"-"9"
  gapY="1"-"9"
>
```

### Box

```tsx
import { Box } from '@radix-ui/themes';

<Box
  as="div" | "span"
  // All shared layout props
>
```

### Container

```tsx
import { Container } from '@radix-ui/themes';

<Container
  size="1" | "2" | "3" | "4"  // max-width: 448px, 688px, 880px, 1136px
  align="left" | "center" | "right"
>
```

### Section

```tsx
import { Section } from '@radix-ui/themes';

<Section
  size="1" | "2" | "3" | "4"  // Vertical padding scale
>
```

## Shared Layout Props

Available on Box, Flex, Grid, Container, Section:

```tsx
// Padding
p="1"-"9"
px="1"-"9"
py="1"-"9"
pt="1"-"9"
pr="1"-"9"
pb="1"-"9"
pl="1"-"9"

// Dimensions
width="100%" | "auto" | string
minWidth="0" | string
maxWidth="100%" | string
height="100%" | "auto" | string
minHeight="0" | string
maxHeight="100%" | string

// Position
position="static" | "relative" | "absolute" | "fixed" | "sticky"
inset="0" | "auto" | string
top="0" | string
right="0" | string
bottom="0" | string
left="0" | string

// Overflow
overflow="visible" | "hidden" | "clip" | "scroll" | "auto"
overflowX="..."
overflowY="..."

// Flex child props
flexBasis="auto" | "0" | string
flexShrink="0" | "1"
flexGrow="0" | "1"

// Grid child props
gridArea="header" | string
gridColumn="1 / 3" | string
gridColumnStart="1" | string
gridColumnEnd="3" | string
gridRow="1 / 3" | string
gridRowStart="1" | string
gridRowEnd="3" | string
```

## Typography Components

### Heading

```tsx
import { Heading } from '@radix-ui/themes';

<Heading
  as="h1" | "h2" | "h3" | "h4" | "h5" | "h6"
  size="1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"
  weight="regular" | "medium" | "bold"
  align="left" | "center" | "right"
  trim="normal" | "start" | "end" | "both"
  truncate={true}
  wrap="wrap" | "nowrap" | "pretty" | "balance"
  color="gray" | "gold" | "bronze" | ... // accent colors
  highContrast={true}
>
```

### Text

```tsx
import { Text } from '@radix-ui/themes';

<Text
  as="p" | "span" | "div" | "label"
  size="1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"
  weight="regular" | "medium" | "bold"
  align="left" | "center" | "right"
  trim="normal" | "start" | "end" | "both"
  truncate={true}
  wrap="wrap" | "nowrap" | "pretty" | "balance"
  color="gray" | ... // accent colors
  highContrast={true}
>
```

### Link

```tsx
import { Link } from '@radix-ui/themes';

<Link
  href="#"
  size="1"-"9"
  weight="regular" | "medium" | "bold"
  underline="auto" | "always" | "hover" | "none"
  color="gray" | ... // accent colors
  highContrast={true}
  truncate={true}
>
```

### Strong, Em

```tsx
import { Strong, Em } from '@radix-ui/themes';

<Text>This is <Strong>important</Strong> and <Em>emphasized</Em>.</Text>
```

## Interactive Components

### Button

```tsx
import { Button } from '@radix-ui/themes';

<Button
  size="1" | "2" | "3" | "4"
  variant="classic" | "solid" | "soft" | "surface" | "outline" | "ghost"
  color="gray" | "gold" | "bronze" | ... // accent colors
  highContrast={true}
  radius="none" | "small" | "medium" | "large" | "full"
  disabled={true}
>
```

### TextField

```tsx
import { TextField } from '@radix-ui/themes';

<TextField.Root
  size="1" | "2" | "3"
  variant="classic" | "surface" | "soft"
  radius="none" | "small" | "medium" | "large" | "full"
  placeholder="..."
  defaultValue="..."
  value={value}
  onChange={handler}
>
  <TextField.Slot side="left">
    <Icon />
  </TextField.Slot>
</TextField.Root>
```

### TextArea

```tsx
import { TextArea } from '@radix-ui/themes';

<TextArea
  size="1" | "2" | "3"
  variant="classic" | "surface" | "soft"
  placeholder="..."
  resize="none" | "vertical" | "horizontal" | "both"
/>
```

### Checkbox

```tsx
import { Checkbox } from '@radix-ui/themes';

<Checkbox
  size="1" | "2" | "3"
  variant="classic" | "surface" | "soft"
  color="..."
  highContrast={true}
  defaultChecked={true}
  checked={checked}
  onCheckedChange={handler}
/>
```

### Switch

```tsx
import { Switch } from '@radix-ui/themes';

<Switch
  size="1" | "2" | "3"
  variant="classic" | "surface" | "soft"
  color="..."
  highContrast={true}
  radius="none" | "small" | "medium" | "large" | "full"
  defaultChecked={true}
  checked={checked}
  onCheckedChange={handler}
/>
```

### Select

```tsx
import { Select } from '@radix-ui/themes';

<Select.Root defaultValue="apple">
  <Select.Trigger placeholder="Pick a fruit" />
  <Select.Content>
    <Select.Group>
      <Select.Label>Fruits</Select.Label>
      <Select.Item value="apple">Apple</Select.Item>
      <Select.Item value="orange">Orange</Select.Item>
    </Select.Group>
    <Select.Separator />
    <Select.Item value="grape">Grape</Select.Item>
  </Select.Content>
</Select.Root>
```

## Container Components

### Card

```tsx
import { Card } from '@radix-ui/themes';

<Card size="1" | "2" | "3" | "4" | "5" variant="surface" | "classic" | "ghost">
  <Flex gap="3" direction="column">
    <Text>Card content</Text>
  </Flex>
</Card>
```

## Responsive Props

All props support responsive values using object syntax:

```tsx
<Flex
  direction={{ initial: "column", sm: "row" }}
  gap={{ initial: "2", md: "4", lg: "6" }}
>

<Grid
  columns={{ initial: "1", sm: "2", md: "3", lg: "4" }}
>

<Text
  size={{ initial: "2", md: "3" }}
>
```

Breakpoints:
- `initial` - 0px+
- `xs` - 520px+
- `sm` - 768px+
- `md` - 1024px+
- `lg` - 1280px+
- `xl` - 1640px+

## Theme Scale Reference

### Spacing/Gap/Padding Scale

| Value | Pixels |
|-------|--------|
| "1" | 4px |
| "2" | 8px |
| "3" | 12px |
| "4" | 16px |
| "5" | 24px |
| "6" | 32px |
| "7" | 40px |
| "8" | 48px |
| "9" | 64px |

### Font Size Scale

| Value | Size |
|-------|------|
| "1" | 12px |
| "2" | 14px |
| "3" | 16px |
| "4" | 18px |
| "5" | 20px |
| "6" | 24px |
| "7" | 28px |
| "8" | 35px |
| "9" | 60px |
