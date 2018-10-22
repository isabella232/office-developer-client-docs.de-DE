---
title: DBEngine.CreateWorkspace-Methode (DAO)
TOCTitle: CreateWorkspace Method
ms:assetid: a7d73771-9420-0448-99e6-d6c4aa78683a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821374(v=office.15)
ms:contentKeyID: 48546888
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052966
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2464426bc7178638e8ebbfc9f5b2f6d1d1b61ca2
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602587"
---
# <a name="dbenginecreateworkspace-method-dao"></a>DBEngine.CreateWorkspace-Methode (DAO)


**Betrifft**: Access 2013 | Office 2013


Erstellt ein neues **[Workspace](workspace-object-dao.md)** -Objekt.

## <a name="syntax"></a>Syntax

*Ausdruck* . CreateWorkspace (***Name***, ***Benutzername***, ***Kennwort***, ***UseType***)

*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.

### <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/Optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Name</p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Ein <strong>String</strong> -Wert, das das neue <strong>Workspace</strong> -Objekt eindeutig benennt. Weitere Informationen zu gültigen <a href="connection-name-property-dao.md">Workspace</a> -Namen finden Sie im Thema zur <strong><strong>Name</strong></strong> -Eigenschaft.  </p></td>
</tr>
<tr class="even">
<td><p>UserName</p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Ein <strong>String</strong> -Wert, der den Besitzer des neuen <strong>Workspace</strong> -Objekts angibt. Weitere Informationen finden Sie im Thema zur <strong>UserName</strong> -Eigenschaft.  </p></td>
</tr>
<tr class="odd">
<td><p>Password</p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Eine <strong>Zeichenfolge</strong>, die das Kennwort für das neue <strong>Arbeitsbereich</strong> -Objekt enthält. Das Kennwort kann bis zu 20 Zeichen lang und alle beliebigen Zeichen außer ASCII-Zeichen 0 (Null) enthalten.  </p>

> [!NOTE]
> <P>[!HINWEIS] Verwenden Sie sichere Kennwörter aus Groß- und Kleinbuchstaben, Zahlen und Symbolen. Unsichere Kennwörter enthalten keine Kombination dieser Elemente. Sicheres Kennwort: Y6dh!et5. Unsicheres Kennwort: Haus27. Verwenden Sie ein sicheres Kennwort, das Sie sich gut merken können, damit Sie es nicht aufschreiben müssen.</P>


</td>
</tr>
<tr class="even">
<td><p>UseType</p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Einer der <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> -Werte.</p>

> [!NOTE]
> <P>[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Festlegen des Arguments Type auf <STRONG>DbUseODBC</STRONG> führt zu einem Laufzeitfehler. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</P>


</td>
</tr>
</tbody>
</table>


<<<<<<< Kopf
### <a name="return-value"></a>Rückgabewert
=======
### <a name="return-value"></a>Rückgabewert
>>>>>>> master

Workspace

## <a name="remarks"></a>Bemerkungen

Wenn Sie mithilfe der **CreateWorkspace** -Methode ein neues **Workspace** -Objekt erstellen, wird eine **Workspace** -Sitzung gestartet, und Sie können in der Anwendung auf das **Workspace** -Objekt verweisen.

**Workspace** -Objekte sind nicht permanent und können nicht auf einem Datenträger gespeichert werden. Nachdem Sie ein **Workspace** -Objekt erstellt haben, können Sie keine Eigenschafteneinstellungen mehr ändern, außer der **Name** -Eigenschaft. Diese können Sie ändern, bevor Sie das **Workspace** -Objekt an die **[Workspaces](workspaces-collection-dao.md)** -Auflistung anfügen.

Es ist nicht erforderlich, das neue **Workspace** -Objekt an eine Auflistung anzufügen, um es verwenden zu können. Ein neu erstelltes **Workspace** -Objekt fügen Sie nur dann an, wenn Sie über die **Workspaces** -Auflistung darauf verweisen müssen.

Wenn Sie ein **Workspace** -Objekt aus der **Workspaces** -Auflistung entfernen möchten, schließen Sie alle geöffneten Datenbanken und Verbindungen. Wenden Sie anschließend die **[Close](connection-close-method-dao.md)** -Methode auf das **Workspace** -Objekt an.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die **CreateWorkspace** -Methode verwendet, um einen Microsoft Access-Arbeitsbereich zu erstellen. Danach werden die Eigenschaften des Arbeitsbereichs aufgelistet.

```vb 
Sub CreateWorkspaceX() 
 
   Dim wrkAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
   DefaultType = dbUseJet 
   ' Create an unnamed Workspace object of the type  
   ' specified by the DefaultType property of DBEngine  
   ' (dbUseJet). 
   Set wrkAcc = CreateWorkspace("", "admin", "") 
 
   ' Enumerate Workspaces collection. 
   Debug.Print "Workspace objects in Workspaces collection:" 
   For Each wrkLoop In Workspaces 
      Debug.Print "  " & wrkLoop.Name 
   Next wrkLoop 
 
   With wrkAcc 
      ' Enumerate Properties collection of Microsoft Access  
      ' workspace. 
      Debug.Print _ 
         "Properties of unnamed Microsoft Access workspace" 
      On Error Resume Next 
      For Each prpLoop In .Properties 
         Debug.Print "  " & prpLoop.Name & " = " & prpLoop 
      Next prpLoop 
      On Error GoTo 0 
   End With 
 
   wrkAcc.Close 
 
End Sub 
 
```
