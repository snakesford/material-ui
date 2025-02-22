---
product: material
title: React Alert component
components: Alert, AlertTitle
githubLabel: 'component: alert'
waiAria: https://www.w3.org/TR/wai-aria-practices/#alert
---

# Alert

<p class="description">An alert displays a short, important message in a way that attracts the user's attention without interrupting the user's task.</p>

**Note:** This component is not documented in the [Material Design guidelines](https://material.io/), but MUI supports it.

{{"component": "modules/components/ComponentLinkHeader.js"}}

## Basic alerts

The alert offers four severity levels that set a distinctive icon and color.

{{"demo": "BasicAlerts.js"}}

## Description

You can use the `AlertTitle` component to display a formatted title above the content.

{{"demo": "DescriptionAlerts.js"}}

## Actions

An alert can have an action, such as a close or undo button.
It is rendered after the message, at the end of the alert.

If an `onClose` callback is provided and no `action` prop is set, a close icon is displayed. The `action` prop can be used to provide an alternative action, for example using a Button or IconButton.

{{"demo": "ActionAlerts.js"}}

### Transition

You can use a [transition component](/components/transitions/) such as `Collapse` to transition the appearance of the alert.

{{"demo": "TransitionAlerts.js"}}

## Icons

The `icon` prop allows you to add an icon to the beginning of the alert component.
This will override the default icon for the specified severity.

You can change the default severity to icon mapping with the `iconMapping` prop. This can be defined globally using [theme customization](/customization/theme-components/#default-props).

Setting the icon prop to `false` will remove the icon altogether.

{{"demo": "IconAlerts.js"}}

## Variants

Two additional variants are available – outlined, and filled:

### Outlined

{{"demo": "OutlinedAlerts.js"}}

### Filled

{{"demo": "FilledAlerts.js"}}

## Toast

You can use the Snackbar to [display a toast](/components/snackbars/#customized-snackbars) with the Alert.

## Color

The `color` prop will override the default color for the specified severity.

{{"demo": "ColorAlerts.js"}}

## Accessibility

(WAI-ARIA: https://www.w3.org/TR/wai-aria-practices/#alert)

When the component is dynamically displayed, the content is automatically announced by most screen readers. At this time, screen readers do not inform users of alerts that are present when the page loads.

Using color to add meaning only provides a visual indication, which will not be conveyed to users of assistive technologies such as screen readers. Ensure that information denoted by the color is either obvious from the content itself (for example the visible text), or is included through alternative means, such as additional hidden text.

Actions must have a tab index of 0 so that they can be reached by keyboard-only users.
