---
title: Recordset.Edit-Methode (DAO)
TOCTitle: Edit Method
ms:assetid: a64d601b-f446-da40-0020-b99110a72872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821175(v=office.15)
ms:contentKeyID: 48546850
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 82dc6e175c7168d5c1b042e85dce7b77aa96b575
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300539"
---
# <a name="recordsetedit-method-dao"></a>Recordset.Edit-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Kopiert den aktuellen Datensatz zur weiteren Bearbeitung aus einem aktualisierbaren **[Recordset](recordset-object-dao.md)**-Objekt in den Kopierpuffer.

## <a name="syntax"></a>Syntax

*Ausdruck* .Edit

*Ausdruck* Eine Variable, die ein **Recordset**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Wenn Sie die **Edit**-Methode verwenden, werden Änderungen, die an den Feldern des aktuellen Datensatzes vorgenommen werden, in den Kopierpuffer kopiert. Speichern Sie die Änderungen mithilfe der **[Update](recordset-update-method-dao.md)** -Methode, nachdem Sie die gewünschten Änderungen an dem Datensatz vorgenommen haben.

Der aktuelle Datensatz bleibt nach der Verwendung von **Edit** aktuell.

> [!NOTE]
> Wenn Sie einen Datensatz bearbeiten und dann durch einen beliebigen Vorgang zu einem anderen Datensatz wechseln, ohne zuerst **Update** zu verwenden, gehen Ihre Änderungen ohne Warnung verloren. Der bearbeitete Datensatz wird außerdem ohne Warnung verworfen, wenn Sie den Recordset schließen oder die Prozedur beenden, die das ****Recordset****- oder das übergeordnete [**Database**](database-object-dao.md)- oder [Connection](connection-object-dao.md)-Objekt deklariert.

Die Verwendung von **Edit** erzeugt in folgenden Fällen einen Fehler:

- Es ist kein aktueller Datensatz vorhanden.

- Das **Connection**-, **Database**- oder **Recordset**-Objekt wurde schreibgeschützt geöffnet.

- Der Datensatz enthält keine aktualisierbaren Felder.

- Das **Database**- oder **Recordset**-Objekt wurde zur exklusiven Verwendung von einem anderen Benutzer geöffnet (Microsoft Access-Arbeitsbereich).

- Ein anderer Benutzer hat die Seite mit Ihrem Datensatz gesperrt (Microsoft Access-Arbeitsbereich).

Ist in einem Microsoft Access-Arbeitsbereich die [**LockEdits**](recordset-lockedits-property-dao.md) -Eigenschafteneinstellung des **Recordset**-Objekts in einer Mehrbenutzerumgebung auf **True** festgelegt (pessimistisch gesperrt), bleibt der Datensatz ab dem Moment gesperrt, in dem **Edit** verwendet wird. Die Sperre wird erst dann aufgehoben, wenn die Aktualisierung abgeschlossen ist. Wenn die **LockEdits**-Eigenschafteneinstellung auf **False** festgelegt ist (optimistisch gesperrt), wird der Datensatz gesperrt und mit dem vorab bearbeiteten Datensatz verglichen, bevor er in der Datenbank aktualisiert wird. Wurde der Datensatz seit dem Verwenden der **Edit**-Methode geändert, schlägt die **Update**-Operation mit einem Laufzeitfehler fehl, falls Sie **OpenRecordset** anwenden, ohne **dbSeeChanges** anzugeben. Standardmäßig verwenden die mit einem Microsoft Access-Datenbankmodul verbundenen ODBC- und installierbare ISAM-Datenbanken immer optimistische Sperren.

> [!NOTE]
> Es muss ein eindeutiger Index für den Datensatz in der zugrunde liegenden Datenquelle vorhanden sein, damit ein Datensatz hinzugefügt, bearbeitet oder gelöscht werden kann. Andernfalls tritt im Aufruf der Methoden **[AddNew](recordset-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)** oder **Edit** in einem Microsoft Access-Arbeitsbereich ein Fehler vom Typ "Berechtigung verweigert" auf.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die **Edit**-Methode verwendet, um die aktuellen Daten durch den angegebenen Namen zu ersetzen. Die EditName-Prozedur ist zum Ausführen dieser Prozedur erforderlich.

```vb
    Sub EditX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     ' Store original data. 
     strOldFirst = rstEmployees!FirstName 
     strOldLast = rstEmployees!LastName 
     
     ' Get new data for record. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed if the user entered something for both fields. 
     If strFirstName <> "" and strLastName <> "" Then 
     ' Update record with new data. 
     EditName rstEmployees, strFirstName, strLastName 
     
     With rstEmployees 
     ' Show old and new data. 
     Debug.Print "Old data: " & strOldFirst & _ 
     " " & strOldLast 
     Debug.Print "New data: " & !FirstName & _ 
     " " & !LastName 
     ' Restore original data because this is a 
     ' demonstration. 
     .Edit 
     !FirstName = strOldFirst 
     !LastName = strOldLast 
     .Update 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub EditName(rstTemp As Recordset, _ 
     strFirst As String, strLast As String) 
     
     ' Make changes to record and set the bookmark to keep 
     ' the same record current. 
     With rstTemp 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Sub
```
