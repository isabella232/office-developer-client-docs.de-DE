---
<<<<<<< HEAD-Titel: CommandText-Eigenschaft (ADO) TOCTitle: CommandText-Eigenschaft (ADO) === Titel: CommandText-Eigenschaft (ADO) TOCTitle: CommandText-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15) Ms:contentKeyID: 48543234 ms.date: 09/18/2015 Mtps_version: Office. 15 f1_keywords:
- ado210.chm1231123 f1_categories:
- Office.Version=v15
---

<<<<<<< Kopf
# <a name="commandtext-property-ado"></a>CommandText-Eigenschaft (ADO)
=======
# <a name="commandtext-property-ado"></a>CommandText-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt den Text eines Befehls an, der an einen Anbieter ausgegeben werden soll.

<<<<<<< Kopf
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Mit dieser Eigenschaft wird ein **String** -Wert festgelegt oder zurückgegeben, der einen Anbieterbefehl enthält, z. B. eine SQL-Anweisung, einen Tabellennamen, eine relative URL oder den Aufruf einer gespeicherten Prozedur. Die Standardeinstellung ist "" (leere Zeichenfolge).

## <a name="remarks"></a>Hinweise

Verwenden Sie die **CommandText** -Eigenschaft, um den Text eines durch ein [Command](command-object-ado.md)-Objekt identifizierten Befehls festzulegen oder zurückzugeben. Gewöhnlich handelt es sich dabei um eine SQL-Anweisung. Möglich ist jedoch auch jede andere vom Anbieter erkannte Befehlsanweisung, wie z. B. ein Aufruf einer gespeicherten Prozedur. Eine SQL-Anweisung muss genau dem Dialekt oder der Version entsprechen, die vom Abfrageprozessor des Anbieters unterstützt werden.

<<<<<<< HEAD, wenn die [Prepared](prepared-property-ado.md) -Eigenschaft des **Command** -Objekts auf **True** festgelegt ist und das **Command** -Objekt an eine offene Verbindung gebunden ist, wenn Sie die **CommandText** -Eigenschaft festlegen, ADO bereitet die Abfrage () d. h., eine kompilierte Form der Abfrage, die vom Anbieter gespeichert ist) Wenn Sie die [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) oder **Open** -Methoden aufrufen.
=== Wenn die [Prepared](prepared-property-ado.md) -Eigenschaft des **Command** -Objekts auf **True** festgelegt ist, und das **Command** -Objekt an eine offene Verbindung gebunden ist, wenn Sie die **CommandText** -Eigenschaft festlegen, bereitet ADO die Abfrage (d. h., eine kompilierte Form der der Abfrage, die vom Anbieter gespeichert ist) Wenn Sie die [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) oder **Open** -Methoden aufrufen.
>>>>>>> master

In Abhängigkeit von der Einstellung für die [CommandType](commandtype-property-ado.md)-Eigenschaft wird die **CommandText** -Eigenschaft möglicherweise von ADO geändert. Sie können die **CommandText** -Eigenschaft jederzeit lesen, um den tatsächlichen Befehlstext anzuzeigen, den ADO bei der Ausführung verwenden wird.

Mit der **CommandText** -Eigenschaft können Sie eine relative URL festlegen oder zurückgeben, die eine Ressource angibt, wie z. B. eine Datei oder ein Verzeichnis. Die Ressource ist relativ zu einem explizit durch eine absolute URL angegebenen Speicherort oder implizit zu einem geöffneten [Connection](connection-object-ado.md)-Objekt.


> [!NOTE]
<<<<<<< Kopf
> <P>[!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider für Internet Publishing</A> automatisch aufgerufen. Weitere Informationen erhalten Sie unter <A href="absolute-and-relative-urls.md">Absolute und relative URLs</A>.</P>
=======
> [!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der [Microsoft OLE DB Provider für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) automatisch aufgerufen. Weitere Informationen finden Sie unter [Absolute und relative URLs](absolute-and-relative-urls.md).
>>>>>>> master


