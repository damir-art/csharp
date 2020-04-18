# XAML
* Все теги можно закрывать закрывающим тегом `<Window> </Window>` или закрывающим слешем `<Window />`.
* Каждый элемент XAML соответствует определённому классу в C#, например `Button` это `System.Windows.Controls.Button`.
* Свойства класса соответствуют атрибутам элемента.
* Элементы интерфейса можно создавать не только с помощью XAML (.xaml), но и с помощью C# (.cs).

## Пример
По нажатию по кнопке, текст из одного текстового поля скопируется в другое текстовое поле, также появится модально окно с данным текстом и новая кнопка:

XAML

    <Grid>
        <TextBox x:Name="TextName" Text="Привет" Width="300" Height="30" VerticalAlignment="Top" Margin="0,20,0,0" FontSize="18"></TextBox>
        <TextBox x:Name="TextProcessing" Width="300" Height="30" VerticalAlignment="Top" Margin="0,70,0,0" FontSize="18"></TextBox>
        <Button x:Name="Send" Width="100" Height="30" VerticalAlignment="Top" Margin="0,120,0,0" Content="Обработать" Click="Send_Click"></Button>
    </Grid>

C#

    private void Send_Click(object sender, RoutedEventArgs e)
    {
        string textName = TextName.Text;
        TextProcessing.Text = textName;

        // Показываем сообщение
        MessageBox.Show(textName);

        // Создаём кнопку
        Button newButton = new Button();
        newButton.Width = 120;
        newButton.Height = 30;
        newButton.Content = "Новая кнопка";
        GridMain.Children.Add(newButton);
    }

## Размеры
Размеры у элементов задаются только числами `"10"`, это делает независимым от устройства. Но можно также задать размер в пикселях, точках, сантиметрах дюймах: `"10 px"`, `"10 in"`, `"10 cm"`, `"10 pt"`.

