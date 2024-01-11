# salesforcemakeringcloud-script-createde
[Salesforce Marketing Cloud] Javascript ServerSide para criação de Data Extension

<script runat="server">
    Platform.Load("core","1.1");
    var DE = "TB_BASE_UNICA_B2C"
    try {
        var obj = {
            "CustomerKey" : Platform.Function.GUID(),
            "Name" : DE,
            "Fields" : [
                { "Name" : "ContactKey", "FieldType" : "Text", "IsPrimaryKey" : true, "IsRequired" : true, "MaxLength" : 150 },
                { "Name" : "Id_ContaGenial", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "ContaDigital", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "FirstName", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "Email", "FieldType" : "EmailAddress", "MaxLength" : 150 },
                { "Name" : "Locale", "FieldType" : "Locale", "MaxLength" : 5 },
                { "Name" : "Celular", "FieldType" : "Phone", "MaxLength" : 50 },                
                { "Name" : "Idade", "FieldType" : "Number" },
                { "Name" : "Cpf", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "DataCadastro", "FieldType" : "Date", "Ordinal" : 2 },
                { "Name" : "DataProxAniversario", "FieldType" : "Date", "Ordinal" : 2 },
                { "Name" : "Score", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "Suitability", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "Status_Suitability", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "Perfil_Investidor", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "Grupo", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "Barra_Comercial", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "Posicao_Total", "FieldType" : "Decimal", "MaxLength" : 23 , "Scale" : 15},
                { "Name" : "AssessorFullName", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "AssessorFirstName", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "AssessorEmail", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "AssessorCelular", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "PrimaryOwner", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "OwnerId", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "Id_FinAcc", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "Id_Acc", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "Id_User", "FieldType" : "Text", "MaxLength" : 150 },
                { "Name" : "CreatedDate", "FieldType" : "Date", "Ordinal" : 2 }                
            ]
        };
        DataExtension.Add(obj);
        Write("(+) Data Extension was created successfully." + "<br>");
    } catch (err) {
        Write("(!) Data Extension was not created. Error message: " + err + "<br>")
    }     
</script>
