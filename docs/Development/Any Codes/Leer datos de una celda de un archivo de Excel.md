# Leer datos de una celda de un archivo de Excel

Leemos un archivo Excel de una ruta y sacamos la hoja, del libro

    ```JAVA
    private FileInputStream archivo;
    private Workbook libroExcel;
    private Sheet hoja;


    public void leerArchivoDeExcel() throws IOException {
        archivo = new FileInputStream("resources/main/archivo.xlsx");
        libroExcel = new XSSFWorkbook(archivo);
        hoja = libroExcel.getSheetAt(0);
    }
    ```

Metodo que lee la celda

    ```JAVA
    public String Celda(String celda) {
        FormulaEvaluator evaluator = wb.getCreationHelper().createFormulaEvaluator();
        CellReference cellReference = new CellReference(celda);
        Row row = sheet.getRow(cellReference.getRow());
        Cell cell = row.getCell(cellReference.getCol());
        CellValue cellValue = evaluator.evaluate(cell);
        switch (cellValue.getCellType()) {
            case Cell.CELL_TYPE_NUMERIC://si la celda es un numero
                return String.valueOf((int) cellValue.getNumberValue());
            case Cell.CELL_TYPE_STRING://si la celda es una cadena de caracteres
                return cellValue.getStringValue();
        }
        return "";
    }
    ```

Invocar el método que lee el dato de la celda

    ```JAVA
    String celdaC3 = Celda("C3");
    ```
