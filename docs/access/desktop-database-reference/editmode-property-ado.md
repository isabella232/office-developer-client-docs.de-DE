---
<<<<<<< HEAD-Titel: EditMode-Eigenschaft (ADO) TOCTitle: EditMode-Eigenschaft (ADO) === Titel: EditMode-Eigenschaft (ADO) TOCTitle: EditMode-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15) Ms:contentKeyID: 48543867 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="editmode-property-ado"></a>EditMode-Eigenschaft (ADO)
=======
# <a name="editmode-property-ado"></a>EditMode-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt den Bearbeitungsstatus des aktuellen Datensatzes an.

<<<<<<< Kopf
## <a name="return-value"></a>Rückgabewert
=======
## <a name="return-value"></a>Rückgabewert
>>>>>>> master

Gibt einen [EditModeEnum](editmodeenum.md)-Wert zurück.

## <a name="remarks"></a>Hinweise

ADO verwaltet einen Bearbeitungspuffer, der dem aktuellen Datensatz zugeordnet ist. Diese Eigenschaft gibt an, ob Änderungen an diesem Puffer vorgenommen wurden oder ob ein neuer Datensatz erstellt wurde. Verwenden Sie die **EditMode** -Eigenschaft, um den Bearbeitungsstatus des aktuellen Datensatzes zu bestimmen. Sie können testen, ob ausstehende Änderungen vorhanden sind, falls ein Bearbeitungsprozess unterbrochen wurde, und bestimmen, ob die [Update](update-method-ado.md)- oder die [CancelUpdate](cancelupdate-method-ado.md)-Methode zu verwenden ist.

Eine ausführlichere Beschreibung der [EditMode](addnew-method-ado.md) -Eigenschaft unter verschiedenen Bearbeitungsbedingungen finden Sie unter der **AddNew**-Methode.

Wenn ein Anruf an [Löschen](delete-method-ado-recordset.md) löscht den Datensatz nicht erfolgreich oder Datensätze in der Datenquelle (aufgrund von referenzielle Integrität Verstöße, beispielsweise), das [Recordset-Objekt](recordset-object-ado.md) im Bearbeitungsmodus bleiben (**EditMode** = **AdEditInProgress **). Dies bedeutet, dass **CancelUpdate** muss, bevor Sie fortfahren aufgerufen werden deaktiviert den aktuellen Datensatz (mit [Verschieben](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md)oder [Schließen](close-method-ado.md), beispielsweise).


> [!NOTE]
> <P><STRONG>EditMode</STRONG> kann nur einen gültigen Wert zurückgeben, wenn ein aktueller Datensatz vorhanden ist. <STRONG>EditMode</STRONG> gibt einen Fehler zurück, wenn <A href="bof-eof-properties-ado.md">BOF oder EOF</A> true ist, oder wenn der aktuelle Datensatz gelöscht wurde.</P>


