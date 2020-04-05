# Программирование Windows Forms

Создадим простейший код, вывод текста при клике по кнопке.

* Кликаем правой кнопкой по форме `Перейти к коду`.
* Или кликаем два раза по кнопке, сразу создастся код-событие клик по кнопке.

Код:

    using System;
    using System.Windows.Forms;

    namespace MetanitForms
    {
        public partial class Form1 : Form
        {
            public Form1()
            {
                InitializeComponent();
            }

            private void button1_Click(object sender, EventArgs e)
            {
                MessageBox.Show("Клик по кнопке!");
            }
        }
    }

* Жмём по клавише `F5` или по зелёной стрелке. Запустится приложение.
* Приложение `.exe` хранится в папках `bin/Debug` или `bin/Release`.