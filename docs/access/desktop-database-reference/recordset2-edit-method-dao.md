---
title: Recordset2.Edit Method (DAO)
TOCTitle: Edit Method
ms:assetid: 34c51eee-274d-3511-b5e2-cb74e4925ec8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192452(v=office.15)
ms:contentKeyID: 48544137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052869
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1255bd4aca0660cb6cb7baece5c569baa5bc1371
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475800"
---
# <a name="recordset2edit-method-dao"></a>Recordset2.Edit Method (DAO)


**Betrifft**: Access 2013 | Office 2013

Kopiert den aktuellen Datensatz aus einem aktualisierbaren **[Recordset](recordset-object-dao.md)** -Objekt zur nachfolgenden Bearbeitung in den Kopierpuffer.

## <a name="syntax"></a>Syntax

*Ausdruck* . Bearbeiten

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Hinweise

Wenn Sie die **Edit** -Methode verwenden, werden an den Feldern des aktuellen Datensatzes vorgenommene Änderungen in den Kopierpuffer kopiert. Nachdem Sie die gewünschten Änderungen am Datensatz vorgenommen haben, verwenden Sie die **[Update](recordset2-update-method-dao.md)** -Methode, um die Änderungen zu speichern.

Der aktuelle Datensatz bleibt nach der Verwendung von **Edit** aktuell.


> [!NOTE]
> <P>[!HINWEIS] Wenn Sie einen Datensatz bearbeiten und dann einen Vorgang durchführen, mit dem Sie zu einem anderen Datensatz wechseln, ohne jedoch zunächst <STRONG>Update</STRONG> zu verwenden, gehen Ihre Änderungen ohne Warnung verloren. Darüber hinaus wird beim Schließen des Recordset-Objekts oder die Prozedur beenden, die das <STRONG>Recordset-Objekt</STRONG> oder das übergeordnete <STRONG><A href="database-object-dao.md">Datenbank-</A></STRONG> oder <STRONG><A href="connection-object-dao.md">Verbindungstyp</A></STRONG> Objekt deklariert, der bearbeitete Datensatz ohne Warnung verworfen.</P>



Die Verwendung von **Edit** erzeugt in folgenden Fällen einen Fehler:

  - Es ist kein aktueller Datensatz vorhanden.

  - Das **Connection** -, **Database** - oder **Recordset** -Objekt wurde schreibgeschützt geöffnet.

  - Der Datensatz enthält keine aktualisierbaren Felder.

  - Das **Database** - oder **Recordset** -Objekt wurde zur exklusiven Verwendung von einem anderen Benutzer geöffnet (Microsoft Access-Arbeitsbereich).

  - Ein anderer Benutzer hat die Seite mit Ihrem Datensatz gesperrt (Microsoft Access-Arbeitsbereich).

Wenn in einem Microsoft Access-Arbeitsbereich die [**LockEdits**](recordset2-lockedits-property-dao.md) -Eigenschafteneinstellung des **Recordset** -Objekts in einer Mehrbenutzerumgebung auf **True** (pessimistisch gesperrt) festgelegt ist, bleibt der Datensatz ab dem Zeitpunkt der Verwendung von **Edit** bis zum Abschluss der Aktualisierung gesperrt. Wenn die **LockEdits** -Eigenschafteneinstellung auf **False** (optimistisch gesperrt) festgelegt ist, wird der Datensatz gesperrt und mit dem vorher bearbeiteten Datensatz verglichen, kurz bevor er in der Datenbank aktualisiert wird. Wenn der Datensatz seit der Verwendung der **Edit** -Methode geändert wurde, tritt beim **Update** -Vorgang ein Laufzeitfehler auf, falls Sie **OpenRecordset** ohne Angabe von **dbSeeChanges** verwenden. Standardmäßig verwenden mit dem Microsoft Access-Datenbankmodul verbundene ODBC- und installierbare ISAM-Datenbanken immer die optimistische Sperrung.


> [!NOTE]
> <P>[!HINWEIS] Um einen Datensatz hinzuzufügen, zu bearbeiten oder zu löschen, muss es einen eindeutigen Index für den Datensatz in der zugrunde liegenden Datenquelle geben. Andernfalls tritt ein "Berechtigung verweigert"-Fehler im <STRONG><A href="recordset2-addnew-method-dao.md">AddNew</A></STRONG> -, <STRONG><A href="fields-delete-method-dao.md">Delete</A></STRONG> - oder <STRONG>Edit</STRONG> -Methodenaufruf in einem Microsoft Access-Arbeitsbereich auf.</P>



## <a name="example"></a>Beispiel

In diesem Beispiel wird die **Edit** -Methode verwendet, um die aktuellen Daten durch den angegebenen Namen zu ersetzen. Die EditName-Prozedur ist zum Ausführen dieser Prozedur erforderlich.

```vb
    Sub EditX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
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
     
    Sub EditName(rstTemp As Recordset2, _ 
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
