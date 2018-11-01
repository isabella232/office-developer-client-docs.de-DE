---
title: Name-Eigenschaft (ADO)
TOCTitle: Name property (ADO)
ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15)
ms:contentKeyID: 48544683
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8be8e1dcb2defacffda92e4a6f60e0c7f7a8f52d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882553"
---
# <a name="name-property-ado"></a><span data-ttu-id="66e17-102">Name-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="66e17-102">Name property (ADO)</span></span>


<span data-ttu-id="66e17-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66e17-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66e17-104">Gibt den Namen eines Objekts an.</span><span class="sxs-lookup"><span data-stu-id="66e17-104">Indicates the name of an object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="66e17-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="66e17-105">Settings and return values</span></span>

<span data-ttu-id="66e17-106">Legt einen **String** -Wert fest, der den Namen eines Objekts oder einer Anwendung angibt, oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="66e17-106">Sets or returns a **String** value that indicates the name of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="66e17-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="66e17-107">Remarks</span></span>

<span data-ttu-id="66e17-108">Verwenden Sie die **Name** -Eigenschaft, um den Namen eines **Command** -, **Property** -, **Field** - oder **Parameter** -Objekts zuzuweisen oder abzurufen.</span><span class="sxs-lookup"><span data-stu-id="66e17-108">Use the **Name** property to assign a name to or retrieve the name of a **Command**, **Property**, **Field**, or **Parameter** object.</span></span>

<span data-ttu-id="66e17-109">Der Wert ist bei einem **Command** -Objekt nicht schreibgeschützt. Bei einem **Property** -Objekt ist der Wert schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="66e17-109">The value is read/write on a **Command** object and read-only on a **Property** object.</span></span>

<span data-ttu-id="66e17-p101">Bei einem **Field** -Objekt ist **Name** in der Regel schreibgeschützt. Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, ist **Name** erst schreibgeschützt, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt festgelegt wurde und der Datenprovider das neue **Field** -Objekt durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="66e17-p101">For a **Field** object, **Name** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Name** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="66e17-p102">Bei **Parameter** -Objekten, die der [Parameters](parameters-collection-ado.md)-Auflistung noch nicht angefügt wurden, ist die **Name** -Eigenschaft nicht schreibgeschützt. Bei angefügten **Parameter** -Objekten und allen sonstigen Objekten ist die **Name** -Eigenschaft schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="66e17-p102">For **Parameter** objects not yet appended to the [Parameters](parameters-collection-ado.md) collection, the **Name** property is read/write. For appended **Parameter** objects and all other objects, the **Name** property is read-only. Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="66e17-115">Sie können die **Name** -Eigenschaft eines Objekts ordinal Bezugnahme abrufen, nach denen Sie auf das Objekt direkt nach Namen verweisen können.</span><span class="sxs-lookup"><span data-stu-id="66e17-115">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name.</span></span> <span data-ttu-id="66e17-116">Beispielsweise wenn rstMain.Properties(20). Name ergibt Updatability, Sie können später auf diese Eigenschaft, wenn Updatability liefert verweisen, Sie können später auf diese Eigenschaft als rstMain.Properties("Updatability") verweisen.</span><span class="sxs-lookup"><span data-stu-id="66e17-116">For example, if rstMain.Properties(20).Name yields Updatability , you can subsequently refer to this property as yields Updatability , you can subsequently refer to this property as rstMain.Properties("Updatability") .</span></span>

