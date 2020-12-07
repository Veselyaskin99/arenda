# Меню

![](https://user-images.githubusercontent.com/74318083/101327940-5bc27b00-38aa-11eb-81fb-1aa85895f9dd.png)
### Код формы "Меню":
namespace Best
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }
        private void button7_Click(object sender, EventArgs e)
        {
            Statistic st = new Statistic();
            st.ShowDialog(this);
        }

        private void btnWorker_Click(object sender, EventArgs e)
        {
            FWorker fWorker = new FWorker();
            fWorker.ShowDialog();  
        }

        private void Form1_Load(object sender, EventArgs e)
        {

        }

        private void button3_Click(object sender, EventArgs e)
        {
            AllContracts all = new AllContracts();
            all.ShowDialog();
        }

        private void button2_Click(object sender, EventArgs e)
        {
            Clients client = new Clients();
            client.ShowDialog();
        }

        private void button4_Click(object sender, EventArgs e)
        {
            Payes pay = new Payes();
            pay.ShowDialog();
        }

        private void button6_Click(object sender, EventArgs e)
        {
            Transport ts = new Transport();
            ts.ShowDialog();
        }
    }
}

# Вкладка "Сотрудники"
![](https://user-images.githubusercontent.com/74318083/101329685-a9d87e00-38ac-11eb-8a22-d3df0d493ea9.png)
### Функционал:
- В textbox можно ввести Имя и в таблице найдется нужный менеджер;
- Вкладка "Добавить сотрудника"(Отображается форма добавления клиента);
- Вкладка "Редактировать / просмотр"(Позволяет открыть форму, с полной информацией о клиенте, где можно ее редактировать;
- При двойном нажатии на строку в таблице, откроется форма с полной информацией о клиенте, где можно ее редактировать;
- Кнопка "Удалить сотрудника" Позволяет удалить сотрудника из таблицы и БД;
### Код формы "Сотрудники":
namespace Best
{
    public partial class FWorker : Form
    {
        Context db;
        public FWorker()
        {
            InitializeComponent();
           
            db = new Context();
            db.Workers.Load();
        }

        private void linkMenu_LinkClicked(object sender, LinkLabelLinkClickedEventArgs e)
        {
            Form1 form1 = new Form1();
            form1.ShowDialog();
            this.Close();
        }

        private void FWorker_Load(object sender, EventArgs e)
        {
                        this.workersTableAdapter.Fill(this._DemidLR8_Class_ContractContextDataSet.Workers);
        }
        private void bcAddWorker(object sender, EventArgs e)
        {
            
            AddWorker addWorker = new AddWorker();
            
            addWorker.ShowDialog();
            this.Close();
        }
        private void dataGridView13_CellContentDoubleClick(object sender, DataGridViewCellEventArgs e)
        {

            int index = dataGridView13.SelectedRows[0].Index;
            int id = 0;
            bool converted = Int32.TryParse(dataGridView13[0, index].Value.ToString(), out id);
            if (converted == false)
                return;

                Workers worker = db.Workers.Find(id);
                currentWorker currentWorker = new currentWorker();
            

                currentWorker.textBox1.Text = worker.Name;
                currentWorker.textBox2.Text = worker.Position;
                currentWorker.textBox3.Text = worker.Phone;
                currentWorker.textBox4.Text = worker.Salary;
                currentWorker.textBox5.Text = worker.Date;

                DialogResult result = currentWorker.ShowDialog(this);

                worker.Name = currentWorker.textBox1.Text;
                worker.Position = currentWorker.textBox2.Text;
                worker.Phone = currentWorker.textBox3.Text;
                worker.Salary = currentWorker.textBox4.Text;
                worker.Date = currentWorker.textBox5.Text;

                db.SaveChanges();
            dataGridView13.Refresh();
            }

        private void button2_Click(object sender, EventArgs e)
        {
            if (dataGridView13.SelectedRows.Count > 0)
            {
                int index = dataGridView13.SelectedRows[0].Index;
                int id = 0;
                bool converted = Int32.TryParse(dataGridView13[0, index].Value.ToString(), out id);
                if (converted == false)
                    return;

                Workers worker = db.Workers.Find(id);
                currentWorker currentWorker = new currentWorker();


                currentWorker.textBox1.Text = worker.Name;
                currentWorker.textBox2.Text = worker.Position;
                currentWorker.textBox3.Text = worker.Phone;
                currentWorker.textBox4.Text = worker.Salary;
                currentWorker.textBox5.Text = worker.Date;

                DialogResult result = currentWorker.ShowDialog(this);

                worker.Name = currentWorker.textBox1.Text;
                worker.Position = currentWorker.textBox2.Text;
                worker.Phone = currentWorker.textBox3.Text;
                worker.Salary = currentWorker.textBox4.Text;
                worker.Date = currentWorker.textBox5.Text;

                

                db.SaveChanges();
                dataGridView13.Refresh();
            }
        }
        private void button3_Click(object sender, EventArgs e)
        {
            if (dataGridView13.SelectedRows.Count > 0)
            {
                int index = dataGridView13.SelectedRows[0].Index;
                int id = 0;
                bool converted = Int32.TryParse(dataGridView13[0, index].Value.ToString(), out id);
                if (converted == false)
                    return;

                Workers worker = db.Workers.Find(id);
                db.Workers.Remove(worker);
                db.SaveChanges();
                dataGridView13.Refresh();
                MessageBox.Show("Удалено");
            }
        }
        private void tbSearchWorker_TextChanged(object sender, EventArgs e)
        {
            dataGridView13.DataSource = db.Workers.Where(x => x.Name.Contains(tbSearchWorker.Text)).ToList();
        }
