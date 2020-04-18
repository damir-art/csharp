# Свойства
Свойства элементов XAML.

* `x:Name="newButton"` - имя элемента
* `Width="100"` - ширина
* `Height="30"` - высота
* `Text="Текстовое поле"` - текст текстового поля
* `Content="Отправить"` - текст на кнопке
* `FontSize="14"` - размер шрифта
* `VerticalAlignment="Center"` - вертикальное выравнивание
* `HorizontalAlignment="Top"` - горизонтальное выравнивание
* `Background="Red"` - фон
* `Margin="0,20,0,0"` - отступ

## Аналог в C#

    Button newButton = new Button();
    newButton.Width = 120;
    newButton.Height = 30;
    newButton.Content = "Новая кнопка";
    newButton.HorizontalAlignment = HorizontalAlignment.Center;
    newButton.Background = new System.Windows.Media.SolidColorBrush(System.Windows.Media.Colors.Red); // Красный

## События
* `Click` - событие