---
title: Document.Container-Eigenschaft (DAO)
TOCTitle: Container Property
ms:assetid: aa1ace1d-f0b8-e0b0-20b6-d3e296254c51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821451(v=office.15)
ms:contentKeyID: 48546940
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053320
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1fcccc6b4a8ddd1122d75d86075e9cd63bd8dd22
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919038"
---
# <a name="documentcontainer-property-dao"></a><span data-ttu-id="b66d8-102">Document.Container-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="b66d8-102">Document.Container property (DAO)</span></span>


<span data-ttu-id="b66d8-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b66d8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b66d8-p101">Gibt den Namen des **[Container](container-object-dao.md)** -Objekts zurück, zu dem ein **Document**-Objekt gehört (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="b66d8-p101">Returns the name of the **[Container](container-object-dao.md)** object to which a **Document** object belongs (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="b66d8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b66d8-106">Syntax</span></span>

<span data-ttu-id="b66d8-107">*Ausdruck* . Container</span><span class="sxs-lookup"><span data-stu-id="b66d8-107">*expression* .Container</span></span>

<span data-ttu-id="b66d8-108">*Ausdruck* Eine Variable, die ein **Document** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b66d8-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="example"></a><span data-ttu-id="b66d8-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b66d8-109">Example</span></span>

<span data-ttu-id="b66d8-110">Dieses Beispiel zeigt die **Container**-Eigenschaft für verschiedene **Document**-Objekte an.</span><span class="sxs-lookup"><span data-stu-id="b66d8-110">This example displays the **Container** property for a variety of **Document** objects.</span></span>

```vb 
Sub ContainerPropertyX() 
 
 Dim dbsNorthwind As Database 
 Dim ctrLoop As Container 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Display the container name for the first Document 
 ' object in each Container object's Documents collection. 
 For Each ctrLoop In dbsNorthwind.Containers 
 Debug.Print "Document: " & ctrLoop.Documents(0).Name 
 Debug.Print " Container = " & _ 
 ctrLoop.Documents(0).Container 
 Next ctrLoop 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

