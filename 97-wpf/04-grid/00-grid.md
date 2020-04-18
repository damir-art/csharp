# Grid
Наиболее мощный и частоиспользуемый контейнер.

Пример:

    <Grid>
        <Grid.RowDefinitions>
            <RowDefinition></RowDefinition>
            <RowDefinition></RowDefinition>
            <RowDefinition></RowDefinition>
        </Grid.RowDefinitions>
        <Grid.ColumnDefinitions>
            <ColumnDefinition></ColumnDefinition>
            <ColumnDefinition></ColumnDefinition>
            <ColumnDefinition></ColumnDefinition>
        </Grid.ColumnDefinitions>
    </Grid>

- `Grid.RowDefinitions` - контейнер для строк сетки
- `Grid.ColumnDefinitions` - контейнер для столбцов сетки

## Атрибуты
### Grid
- `ShowGridLines="True"` - показать линии сетки

### Размеры ColumnDefinition и RowDefinition
- `ColumnDefinition Width="Auto"` - размер столбца по содержимому
- `ColumnDefinition Width="20"` - абсолютный размер
- `RowDefinition Height="Auto"` - размер по содержимому
- `RowDefinition Height="20"` - абсолютный размер
- `ColumnDefinition Width="*"`, `ColumnDefinition Width="0.25*"` - первый столб займет 75% ширины, второй 25%

## Добавляем элементы
После `</Grid.ColumnDefinitions>` вставляем:

    <Button Grid.Column="0" Grid.Row="0" Content="Строка 0 Столбец 0" />
    <Button Grid.Column="0" Grid.Row="1" Grid.ColumnSpan="3" Content="Объединение трех столбцов" />
    <Button Grid.Column="2" Grid.Row="2" Content="Строка 2 Столбец 2" />

- Grid.Column - столбец сетки
- Grid.Row - строка сетки
- ColumnSpan - объединение столбцов
