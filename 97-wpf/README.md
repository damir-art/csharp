# WPF фреймворк
    Файл > Создать > Проект >
    Приложение WPF (.NET Framework) > Далее > Создать

* Элементы из панели элементов, можно переносить в `MainWindow`.
* `MainWindow.xaml` - вкладка с UI
* `MainWindow.xaml.cs` - вкладка с кодом приложения, здесь прописывается функционал для всех элементов программы

Примеры кода, значения свойствам можно добавлять во вкладку `XAML` (как в HTML), либо в файл `MainWindow.xaml.cs` (как код программирования).

## XAML
    Title="Обработка текста"
    Height="398" Width="600"
    ResizeMode="NoResize"
    Topmost="True" Icon="txt.png"
    WindowStartupLocation="CenterScreen">

* `Topmost="True"` - всегда поверх других программ
* `WindowState="Maximized"` - состояние окна программы: раскрыто, свернуто, нормально
* `Icon="txt.png` - иконка программы, в проекте создаем папку и помещаем туда иконку

## MainWindow.xaml.cs

    // Конструктор, сработает при старте программы
    public MainWindow()
    {
        InitializeComponent();
        
        // Заголовок программы
        this.Title = "Всем привет!";
        
        // Расположение программы при старте, по центру
        this.WindowStartupLocation = WindowStartupLocation.CenterScreen;
        
        // Отключить изменение размеров окна программы
        this.ResizeMode = ResizeMode.NoResize;
    }

## Сетки
* Grid
* StackPanel - элементы друг за другом в столбик или в ряд
* Canvas - свободное расположение элементов

Код:

    <StackPanel Orientation="Vertical">
        <Label x:Name="first_text" Content="Заголовок" HorizontalAlignment="Center" FontSize="30" FontWeight="Bold"/>
        <Label x:Name="label1" Content="Введите текст" HorizontalAlignment="Center" />
        <TextBox x:Name="userInput" Height="23" TextWrapping="Wrap" FontSize="14" HorizontalAlignment="Center" Width="300" />
        <Button x:Name="btnMessageBox" Content="Отправить" Width="100" Margin="0, 10"/>
    </StackPanel>

## Обработчики событий

    <Button x:Name="btnMessageBox" Content="Отправить" Width="100" Margin="0, 10" Click="btnMessageBox_Click"/>

    private void btnMessageBox_Click(object sender, RoutedEventArgs e)
    {
        MessageBox.Show("Обработчик события клик");
    }