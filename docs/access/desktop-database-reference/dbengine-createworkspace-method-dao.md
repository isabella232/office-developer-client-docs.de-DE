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
ms.openlocfilehash: 7e56fa340ceedd33fbd7f628af0acffee5c32438
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997937"
---
# <a name="dbenginecreateworkspace-method-dao"></a><span data-ttu-id="70517-102">DBEngine.CreateWorkspace-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="70517-102">DBEngine.CreateWorkspace method (DAO)</span></span>

<span data-ttu-id="70517-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70517-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70517-104">Erstellt ein neues **[Workspace](workspace-object-dao.md)** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="70517-104">Creates a new **[Workspace](workspace-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="70517-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="70517-105">Syntax</span></span>

<span data-ttu-id="70517-106">*Ausdruck* . CreateWorkspace (***Name***, ***Benutzername***, ***Kennwort***, ***UseType***)</span><span class="sxs-lookup"><span data-stu-id="70517-106">*expression* .CreateWorkspace(***Name***, ***UserName***, ***Password***, ***UseType***)</span></span>

<span data-ttu-id="70517-107">*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="70517-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="70517-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="70517-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70517-109">Name</span><span class="sxs-lookup"><span data-stu-id="70517-109">Name</span></span></p></th>
<th><p><span data-ttu-id="70517-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="70517-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="70517-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="70517-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="70517-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70517-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70517-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="70517-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="70517-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="70517-114">Required</span></span></p></td>
<td><p><span data-ttu-id="70517-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="70517-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="70517-p101">Ein <strong>String</strong> -Wert, das das neue <strong>Workspace</strong> -Objekt eindeutig benennt. Weitere Informationen zu gültigen <a href="connection-name-property-dao.md">Workspace</a> -Namen finden Sie im Thema zur <strong><strong>Name</strong></strong> -Eigenschaft.  </span><span class="sxs-lookup"><span data-stu-id="70517-p101">A <strong>String</strong> that uniquely names the new <strong>Workspace</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Workspace</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70517-118"><em>UserName</em></span><span class="sxs-lookup"><span data-stu-id="70517-118"><em>UserName</em></span></span></p></td>
<td><p><span data-ttu-id="70517-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="70517-119">Required</span></span></p></td>
<td><p><span data-ttu-id="70517-120"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="70517-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="70517-p102">Ein <strong>String</strong> -Wert, der den Besitzer des neuen <strong>Workspace</strong> -Objekts angibt. Weitere Informationen finden Sie im Thema zur <strong>UserName</strong> -Eigenschaft.  </span><span class="sxs-lookup"><span data-stu-id="70517-p102">A <strong>String</strong> that identifies the owner of the new <strong>Workspace</strong> object. See the <strong>UserName</strong> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70517-123"><em>Password</em></span><span class="sxs-lookup"><span data-stu-id="70517-123"><em>Password</em></span></span></p></td>
<td><p><span data-ttu-id="70517-124">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="70517-124">Required</span></span></p></td>
<td><p><span data-ttu-id="70517-125"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="70517-125"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="70517-p103">Eine <strong>Zeichenfolge</strong>, die das Kennwort für das neue <strong>Arbeitsbereich</strong> -Objekt enthält. Das Kennwort kann bis zu 20 Zeichen lang und alle beliebigen Zeichen außer ASCII-Zeichen 0 (Null) enthalten.  </span><span class="sxs-lookup"><span data-stu-id="70517-p103">A <strong>String</strong> containing the password for the new <strong>Workspace</strong> object. The password can be up to 20 characters long and can include any characters except ASCII character 0 (null).</span></span></p>
<p><span data-ttu-id="70517-128"><strong>Hinweis</strong>: Verwenden Sie sichere Kennwörter, die Groß- und Kleinbuchstaben, Zahlen und Symbole kombinieren.</span><span class="sxs-lookup"><span data-stu-id="70517-128"><strong>NOTE</strong>: Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="70517-129">Unsichere Kennwörter enthalten keine Kombination dieser Elemente.</span><span class="sxs-lookup"><span data-stu-id="70517-129">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="70517-130">Sicheres Kennwort: Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="70517-130">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="70517-131">Unsicheres Kennwort: Haus27.</span><span class="sxs-lookup"><span data-stu-id="70517-131">Weak password: House27.</span></span> <span data-ttu-id="70517-132">Verwenden Sie ein sicheres Kennwort, das Sie sich gut merken können, damit Sie es nicht aufschreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="70517-132">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70517-133"><em>UseType</em></span><span class="sxs-lookup"><span data-stu-id="70517-133"><em>UseType</em></span></span></p></td>
<td><p><span data-ttu-id="70517-134">Optional</span><span class="sxs-lookup"><span data-stu-id="70517-134">Optional</span></span></p></td>
<td><p><span data-ttu-id="70517-135"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="70517-135"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="70517-136">Einer der <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> -Werte.</span><span class="sxs-lookup"><span data-stu-id="70517-136">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<p><span data-ttu-id="70517-137"><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="70517-137"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="70517-138">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="70517-138">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="70517-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70517-139">Return value</span></span>

<span data-ttu-id="70517-140">Workspace</span><span class="sxs-lookup"><span data-stu-id="70517-140">Workspace</span></span>

## <a name="remarks"></a><span data-ttu-id="70517-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70517-141">Remarks</span></span>

<span data-ttu-id="70517-142">Wenn Sie mithilfe der **CreateWorkspace** -Methode ein neues **Workspace** -Objekt erstellen, wird eine **Workspace** -Sitzung gestartet, und Sie können in der Anwendung auf das **Workspace** -Objekt verweisen.</span><span class="sxs-lookup"><span data-stu-id="70517-142">Once you use the **CreateWorkspace** method to create a new **Workspace** object, a **Workspace** session is started, and you can refer to the **Workspace** object in your application.</span></span>

<span data-ttu-id="70517-p106">**Workspace** -Objekte sind nicht permanent und können nicht auf einem Datenträger gespeichert werden. Nachdem Sie ein **Workspace** -Objekt erstellt haben, können Sie keine Eigenschafteneinstellungen mehr ändern, außer der **Name** -Eigenschaft. Diese können Sie ändern, bevor Sie das **Workspace** -Objekt an die **[Workspaces](workspaces-collection-dao.md)** -Auflistung anfügen.</span><span class="sxs-lookup"><span data-stu-id="70517-p106">**Workspace** objects aren't permanent, and you can't save them to disk. Once you create a **Workspace** object, you can't alter any of its property settings, except for the **Name** property, which you can modify before appending the **Workspace** object to the **[Workspaces](workspaces-collection-dao.md)** collection.</span></span>

<span data-ttu-id="70517-p107">Es ist nicht erforderlich, das neue **Workspace** -Objekt an eine Auflistung anzufügen, um es verwenden zu können. Ein neu erstelltes **Workspace** -Objekt fügen Sie nur dann an, wenn Sie über die **Workspaces** -Auflistung darauf verweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="70517-p107">You don't have to append the new **Workspace** object to a collection before you can use it. You append a newly created **Workspace** object only if you need to refer to it through the **Workspaces** collection.</span></span>

<span data-ttu-id="70517-147">Wenn Sie ein **Workspace** -Objekt aus der **Workspaces** -Auflistung entfernen möchten, schließen Sie alle geöffneten Datenbanken und Verbindungen. Wenden Sie anschließend die **[Close](connection-close-method-dao.md)** -Methode auf das **Workspace** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="70517-147">To remove a **Workspace** object from the **Workspaces** collection, close all open databases and connections and then use the **[Close](connection-close-method-dao.md)** method on the **Workspace** object.</span></span>

## <a name="example"></a><span data-ttu-id="70517-148">Beispiel</span><span class="sxs-lookup"><span data-stu-id="70517-148">Example</span></span>

<span data-ttu-id="70517-p108">In diesem Beispiel wird die **CreateWorkspace** -Methode verwendet, um einen Microsoft Access-Arbeitsbereich zu erstellen. Danach werden die Eigenschaften des Arbeitsbereichs aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="70517-p108">This example uses the **CreateWorkspace** method to createMicrosoft Access workspace. It then lists the properties of the workspace.</span></span>

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

