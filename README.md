# JExcel

Descrição | Description 
"Biblioteca feita com intuito de melhorar a ultilização de arquivos .xls com java e JTable"
"Library created to improve the use of .xls files with java and JTable"

Comments | Observações
*Compatible with Excel 97 - 2003 | Compativel com Excel 97 - 2003
*Need to import lib jxl          | Necessita de importação da lib jxl

Examples | Exemplos 

Ex : Update and Set elemenst of excel | Atualiza variavel do excel

JExcel e = new JExcel();
        e.setValueExcel("Teste",1,0, new File("C:\\Users\\jhonata.de.b.xavier\\Desktop\\JExcel.xls"), "Sheet1");
        
Ex : Read all the elements of excel | Ler todos os elementos do excel

        JExcel excel = new JExcel();
        excel.setFileLocal_xls("C:\\Users\\jhonata.de.b.xavier\\Documents\\NetBeansProjects\\GeracaoDMassa.xls");
        for (int j = 1; j < excel.getSizeRows(); j++) {
        for (int i = 0; i < excel.getSizeColumns(); i++) {
        System.out.print(excel.getValueExcel(j,i)+" ");
        }
            System.out.println("");
     }

Ex: Import from .xls to Jtable | Importação de .xls para Jtable

        if(exel.fileChosseXLS())
          for (int t = 1; t < exel.getSizeRows(); t++) 
            model.addRow((Object[]) exel.Rows_inObjectArray(jTable.getColumnCount(),t))

Ex :Export | Exportação

        String local = exel.fileChosseOutputLocal();
            if(local != null)
            exel.Jtable_inXLS(jTable, local);

Solution | Soluções de Erros :

- Always check if the location of the file is different from null
- Check the .xls file compatibility
- Some machines may need permission from the administrator to run the application

- Sempre verificar se o local do arquivo e diferente de null
- Verificar a compatibilidade do arquivo .xls        
- Algumas maquina podem precisa de permissão do admistrador para rodar a aplicação   


