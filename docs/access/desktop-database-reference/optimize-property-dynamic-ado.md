---
title: Optimize (dynamische Eigenschaft) (ADO)
TOCTitle: Optimize Property--Dynamic (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7276e642e15137bdcfcb939330a3642d96e9a5a2
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605177"
---
# <a name="optimize-property--dynamic-ado"></a><span data-ttu-id="b3024-102">Optimize (dynamische Eigenschaft) (ADO)</span><span class="sxs-lookup"><span data-stu-id="b3024-102">Optimize Property--Dynamic (ADO)</span></span>


<span data-ttu-id="b3024-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3024-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b3024-104">Gibt an, ob für ein Feld ein Index erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3024-104">Specifies whether an index should be created on a field.</span></span>

<span data-ttu-id="b3024-105"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="b3024-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="b3024-106">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b3024-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="b3024-107">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b3024-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="b3024-108">master</span><span class="sxs-lookup"><span data-stu-id="b3024-108">master</span></span>

<span data-ttu-id="b3024-109">Legt einen **Boolean** -Wert fest, der angibt, ob ein Index erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3024-109">Sets or returns a **Boolean** value that indicates whether an index should be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3024-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b3024-110">Remarks</span></span>

<span data-ttu-id="b3024-p101">Ein Index kann die Leistung von Operationen verbessern, bei denen Werte in einem [Recordset](recordset-object-ado.md) gesucht oder sortiert werden. Der Index ist in ADO integriert, Sie können nicht explizit darauf zugreifen oder ihn in der Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="b3024-p101">An index can improve the performance of operations that find or sort values in a [Recordset](recordset-object-ado.md). The index is internal to ADO — you cannot explicitly access or use it in your application.</span></span>

<span data-ttu-id="b3024-p102">Legen Sie die **Optimize** -Eigenschaft auf **True** fest, um einen Index für ein Feld zu erstellen. Legen Sie diese Eigenschaft auf **False** fest, um den Index zu löschen.</span><span class="sxs-lookup"><span data-stu-id="b3024-p102">To create an index on a field, set the **Optimize** property to **True**. To delete the index, set this property to **False**.</span></span>

<span data-ttu-id="b3024-115">**Optimize** ist eine dynamische Eigenschaft, die der [Properties](field-object-ado.md)-Auflistung des [Field](properties-collection-ado.md)-Objekts angefügt wird, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b3024-115">**Optimize** is a dynamic property appended to the [Field](field-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

<span data-ttu-id="b3024-116">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="b3024-116">**Usage**</span></span>

```vb
    Dim rs As New Recordset
    Dim fld As Field
    rs.CursorLocation = adUseClient      'Enable index creation
    rs.Fields.Append "Field1", adChar, 35, adFldIsNullable
    rs.Open
    Set fld = rs.Fields(0)
    fld.Properties("Optimize") = True    'Create an index
    fld.Properties("Optimize") = False   'Delete an index
```
