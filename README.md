# WindowsFormApp1
Trabalhando com Windows Form

using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace WindowsFormsApp1
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }
        //Declarar variaveis globais
        int anoNasc, idade;
        private void btnEnviar_Click(object sender, EventArgs e)
        {
          //Ao clicar no botão, pegue o texto do txtNome e 
            //atribuir o valor ao lblStatus
            lblStatus.Text = "Boa Tarde!" +txtNome.Text;

  //Atribuir o valor do txtAno para a variavel
            //anoNasc

  anoNasc = Convert.ToInt32(txtAno.Text);
            //idade = 2024 - anoNasc
            idade = DateTime.Now.Year - anoNasc;
            label20.Text = idade.ToString()+" anos.";
        }

  private void btnLimpar_Click(object sender, EventArgs e)
        {
            //Limpar os campos
            txtNome.Clear();
            lblStatus.Text = "Boa Tarde!";
            //lblStatus.Text = string.Empty;
            label20.Text = "";
            txtNome.Focus();
        }

  private void lblStatus_Click(object sender, EventArgs e)
        {

  }
}
}
========================================================================================================================================================================================

{
    internal static class Program
    {
        /// <summary>
        /// Ponto de entrada principal para o aplicativo.
        /// </summary>
        [STAThread]
        static void Main()
        {
            Application.EnableVisualStyles();
            Application.SetCompatibleTextRenderingDefault(false);
            Application.Run(new Form1());
        }
    }
}
