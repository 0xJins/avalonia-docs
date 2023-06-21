# Styling

The most obvious difference from other XAML frameworks is in its styling system. There are two ways of styling controls in Avalonia:

- A [`Style`](../../concepts/styling) is a CSS-like style. Styles aren't stored in a `Resources` collection as in WPF, they are stored in a separate `Styles` collection.
- A [`ControlTheme`](../../concepts/controlthemes) is similar to a WPF `Style` and is usually used to create themes for lookless controls

## Example

The following code shows a `UserControl` which defines its own CSS-like style.

```markup
<UserControl>
    <UserControl.Styles>
        <!-- Make TextBlocks with the h1 style class have a font size of 24 points -->
        <Style Selector="TextBlock.h1">
            <Setter Property="FontSize" Value="24"/>
        </Style>
    </UserControl.Styles>
    <TextBlock Classes="h1">Header</TextBlock>
<UserControl>
```

