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
# <a name="dbenginecreateworkspace-method-dao"></a><span data-ttu-id="8a286-102">DBEngine.CreateWorkspace-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="8a286-102">DBEngine.CreateWorkspace Method (DAO)</span></span>


<span data-ttu-id="8a286-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a286-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="8a286-104">Erstellt ein neues **[Workspace](workspace-object-dao.md)** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8a286-104">Creates a new **[Workspace](workspace-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a286-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a286-105">Syntax</span></span>

<span data-ttu-id="8a286-106">*Ausdruck* . CreateWorkspace (***Name***, ***Benutzername***, ***Kennwort***, ***UseType***)</span><span class="sxs-lookup"><span data-stu-id="8a286-106">*expression* .CreateWorkspace(***Name***, ***UserName***, ***Password***, ***UseType***)</span></span>

<span data-ttu-id="8a286-107">*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8a286-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="8a286-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a286-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8a286-109">Name</span><span class="sxs-lookup"><span data-stu-id="8a286-109">Name</span></span></p></th>
<th><p><span data-ttu-id="8a286-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="8a286-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="8a286-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8a286-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="8a286-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a286-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a286-113">Name</span><span class="sxs-lookup"><span data-stu-id="8a286-113">Name</span></span></p></td>
<td><p><span data-ttu-id="8a286-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8a286-114">Required</span></span></p></td>
<td><p><span data-ttu-id="8a286-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="8a286-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="8a286-p101">Ein <strong>String</strong> -Wert, das das neue <strong>Workspace</strong> -Objekt eindeutig benennt. Weitere Informationen zu gültigen <a href="connection-name-property-dao.md">Workspace</a> -Namen finden Sie im Thema zur <strong><strong>Name</strong></strong> -Eigenschaft.  </span><span class="sxs-lookup"><span data-stu-id="8a286-p101">A <strong>String</strong> that uniquely names the new <strong>Workspace</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Workspace</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a286-118">UserName</span><span class="sxs-lookup"><span data-stu-id="8a286-118">UserName</span></span></p></td>
<td><p><span data-ttu-id="8a286-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8a286-119">Required</span></span></p></td>
<td><p><span data-ttu-id="8a286-120"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="8a286-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="8a286-p102">Ein <strong>String</strong> -Wert, der den Besitzer des neuen <strong>Workspace</strong> -Objekts angibt. Weitere Informationen finden Sie im Thema zur <strong>UserName</strong> -Eigenschaft.  </span><span class="sxs-lookup"><span data-stu-id="8a286-p102">A <strong>String</strong> that identifies the owner of the new <strong>Workspace</strong> object. See the <strong>UserName</strong> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a286-123">Password</span><span class="sxs-lookup"><span data-stu-id="8a286-123">Password</span></span></p></td>
<td><p><span data-ttu-id="8a286-124">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8a286-124">Required</span></span></p></td>
<td><p><span data-ttu-id="8a286-125"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="8a286-125"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="8a286-p103">Eine <strong>Zeichenfolge</strong>, die das Kennwort für das neue <strong>Arbeitsbereich</strong> -Objekt enthält. Das Kennwort kann bis zu 20 Zeichen lang und alle beliebigen Zeichen außer ASCII-Zeichen 0 (Null) enthalten.  </span><span class="sxs-lookup"><span data-stu-id="8a286-p103">A <strong>String</strong> containing the password for the new <strong>Workspace</strong> object. The password can be up to 20 characters long and can include any characters except ASCII character 0 (null).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="8a286-p104">[!HINWEIS] Verwenden Sie sichere Kennwörter aus Groß- und Kleinbuchstaben, Zahlen und Symbolen. Unsichere Kennwörter enthalten keine Kombination dieser Elemente. Sicheres Kennwort: Y6dh!et5. Unsicheres Kennwort: Haus27. Verwenden Sie ein sicheres Kennwort, das Sie sich gut merken können, damit Sie es nicht aufschreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="8a286-p104">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></P>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a286-133">UseType</span><span class="sxs-lookup"><span data-stu-id="8a286-133">UseType</span></span></p></td>
<td><p><span data-ttu-id="8a286-134">Optional</span><span class="sxs-lookup"><span data-stu-id="8a286-134">Optional</span></span></p></td>
<td><p><span data-ttu-id="8a286-135"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8a286-135"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8a286-136">Einer der <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> -Werte.</span><span class="sxs-lookup"><span data-stu-id="8a286-136">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="8a286-137">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8a286-137">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="8a286-138">Festlegen des Arguments Type auf <STRONG>DbUseODBC</STRONG> führt zu einem Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="8a286-138">Setting the type argument to <STRONG>dbUseODBC</STRONG> will result in a run-time error.</span></span> <span data-ttu-id="8a286-139">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8a286-139">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


</td>
</tr>
</tbody>
</table>


<span data-ttu-id="8a286-140"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="8a286-140"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="8a286-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a286-141">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="8a286-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a286-142">Return value</span></span>
>>>>>>> <span data-ttu-id="8a286-143">master</span><span class="sxs-lookup"><span data-stu-id="8a286-143">master</span></span>

<span data-ttu-id="8a286-144">Workspace</span><span class="sxs-lookup"><span data-stu-id="8a286-144">Workspace</span></span>

## <a name="remarks"></a><span data-ttu-id="8a286-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a286-145">Remarks</span></span>

<span data-ttu-id="8a286-146">Wenn Sie mithilfe der **CreateWorkspace** -Methode ein neues **Workspace** -Objekt erstellen, wird eine **Workspace** -Sitzung gestartet, und Sie können in der Anwendung auf das **Workspace** -Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="8a286-146">Once you use the **CreateWorkspace** method to create a new **Workspace** object, a **Workspace** session is started, and you can refer to the **Workspace** object in your application.</span></span>

<span data-ttu-id="8a286-p106">**Workspace** -Objekte sind nicht permanent und können nicht auf einem Datenträger gespeichert werden. Nachdem Sie ein **Workspace** -Objekt erstellt haben, können Sie keine Eigenschafteneinstellungen mehr ändern, außer der **Name** -Eigenschaft. Diese können Sie ändern, bevor Sie das **Workspace** -Objekt an die **[Workspaces](workspaces-collection-dao.md)** -Auflistung anfügen.</span><span class="sxs-lookup"><span data-stu-id="8a286-p106">**Workspace** objects aren't permanent, and you can't save them to disk. Once you create a **Workspace** object, you can't alter any of its property settings, except for the **Name** property, which you can modify before appending the **Workspace** object to the **[Workspaces](workspaces-collection-dao.md)** collection.</span></span>

<span data-ttu-id="8a286-p107">Es ist nicht erforderlich, das neue **Workspace** -Objekt an eine Auflistung anzufügen, um es verwenden zu können. Ein neu erstelltes **Workspace** -Objekt fügen Sie nur dann an, wenn Sie über die **Workspaces** -Auflistung darauf verweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="8a286-p107">You don't have to append the new **Workspace** object to a collection before you can use it. You append a newly created **Workspace** object only if you need to refer to it through the **Workspaces** collection.</span></span>

<span data-ttu-id="8a286-151">Wenn Sie ein **Workspace** -Objekt aus der **Workspaces** -Auflistung entfernen möchten, schließen Sie alle geöffneten Datenbanken und Verbindungen. Wenden Sie anschließend die **[Close](connection-close-method-dao.md)** -Methode auf das **Workspace** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8a286-151">To remove a **Workspace** object from the **Workspaces** collection, close all open databases and connections and then use the **[Close](connection-close-method-dao.md)** method on the **Workspace** object.</span></span>

## <a name="example"></a><span data-ttu-id="8a286-152">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8a286-152">Example</span></span>

<span data-ttu-id="8a286-p108">In diesem Beispiel wird die **CreateWorkspace** -Methode verwendet, um einen Microsoft Access-Arbeitsbereich zu erstellen. Danach werden die Eigenschaften des Arbeitsbereichs aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8a286-p108">This example uses the **CreateWorkspace** method to createMicrosoft Access workspace. It then lists the properties of the workspace.</span></span>

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

