---
title: AbsolutePage-Eigenschaft (ADO)
TOCTitle: AbsolutePage property (ADO)
ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15)
ms:contentKeyID: 48547288
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a0ad4caa6e31b6de39904016cd848e12690f72e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705260"
---
# <a name="absolutepage-property-ado"></a><span data-ttu-id="a68d2-102">AbsolutePage-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="a68d2-102">AbsolutePage property (ADO)</span></span>

<span data-ttu-id="a68d2-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a68d2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a68d2-104">Gibt an, auf welcher Seite sich der aktuelle Datensatz befindet.</span><span class="sxs-lookup"><span data-stu-id="a68d2-104">Indicates on which page the current record resides.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a68d2-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="a68d2-105">Settings and return values</span></span>

<span data-ttu-id="a68d2-106">Legt fest oder gibt einen **Long** -Wert von 1 bis die Anzahl der Seiten im [Recordset](recordset-object-ado.md) -Objekt ([PageCount](pagecount-property-ado.md)) oder einen der Werte [PositionEnum](positionenum.md) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a68d2-106">Sets or returns a **Long** value from 1 to the number of pages in the [Recordset](recordset-object-ado.md) object ([PageCount](pagecount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a68d2-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a68d2-107">Remarks</span></span>

<span data-ttu-id="a68d2-p101">Mit dieser Eigenschaft kann die Nummer der Seite identifiziert werden, auf der sich der aktuelle Datensatz befindet. Sie verwendet die [PageSize](pagesize-property-ado.md)-Eigenschaft, um die Gesamtzahl von Rowsets des **Recordset** -Objekts logisch in Seitenblöcke aufzuteilen, die jeweils die Anzahl von Datensätzen gemäß **PageSize** enthalten (außer der letzten Seite, die weniger Datensätze haben kann). Die entsprechende Funktionalität muss vom Anbieter unterstützt werden, damit diese Eigenschaft verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a68d2-p101">This property can be used to identify the page number on which the current record is located. It uses the [PageSize](pagesize-property-ado.md) property to logically divide the total rowset count of the **Recordset** object into a series of pages, each of which has the number of records equal to **PageSize** (except for the last page, which may have fewer records). The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="a68d2-111">Beim Abrufen oder Festlegen der **AbsolutePage** -Eigenschaft verwendet ADO die [AbsolutePosition](absoluteposition-property-ado.md)- und die [PageSize](pagesize-property-ado.md)-Eigenschaft wie folgt zusammen:</span><span class="sxs-lookup"><span data-stu-id="a68d2-111">When getting or setting the **AbsolutePage** property, ADO uses the [AbsolutePosition](absoluteposition-property-ado.md) property and the [PageSize](pagesize-property-ado.md) property together as follows:</span></span>

- <span data-ttu-id="a68d2-112">Zum Abrufen von **AbsolutePage** ruft ADO zuerst die **AbsolutePosition** -Eigenschaft ab und dividiert den Wert dann durch die **PageSize** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a68d2-112">To get the **AbsolutePage**, ADO first retrieves the **AbsolutePosition**, and then divides it by the **PageSize**.</span></span>

- <span data-ttu-id="a68d2-113">Zum Festlegen von **AbsolutePage** verschiebt ADO die **AbsolutePosition** -Eigenschaft wie folgt: **PageSize** wird mit dem neuen Wert von **AbsolutePage** multipliziert, und dann wird 1 addiert.</span><span class="sxs-lookup"><span data-stu-id="a68d2-113">To set the **AbsolutePage**, ADO moves the **AbsolutePosition** as follows: it multiplies the **PageSize** by the new **AbsolutePage** value and then adds 1 to the value.</span></span> <span data-ttu-id="a68d2-114">Daher wird die aktuelle Position im **Recordset-Objekt** nach dem erfolgreichen festlegen **AbsolutePage** der erste Datensatz in dieser Seite.</span><span class="sxs-lookup"><span data-stu-id="a68d2-114">As a result, the current position in the **Recordset** after successfully setting **AbsolutePage** is the first record in that page.</span></span>

<span data-ttu-id="a68d2-p103">**AbsolutePage** ist wie die **AbsolutePosition** -Eigenschaft 1-basiert und entspricht 1, wenn der aktuelle Datensatz der erste Datensatz im **Recordset** -Objekt ist. Legen Sie diese Eigenschaft fest, um zum ersten Datensatz einer bestimmten Seite zu navigieren. Die Gesamtseitenanzahl rufen Sie von der **PageCount** -Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="a68d2-p103">Like the **AbsolutePosition** property, **AbsolutePage** is 1-based and equals 1 when the current record is the first record in the **Recordset**. Set this property to move to the first record of a particular page. Obtain the total number of pages from the **PageCount** property.</span></span>

