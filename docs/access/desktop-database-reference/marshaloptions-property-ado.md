---
title: MarshalOptions-Eigenschaft (ADO)
TOCTitle: MarshalOptions Property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f290f2f4fb4820fb01d3a63aef7bcfbfa7c1f035
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475197"
---
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="e4646-102">MarshalOptions-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="e4646-102">MarshalOptions Property (ADO)</span></span>


<span data-ttu-id="e4646-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e4646-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e4646-104">Gibt die Datensätze an, die wieder zurück zum Server gemarshallt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e4646-104">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e4646-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e4646-105">Settings And Return Values</span></span>

<span data-ttu-id="e4646-p101">Legt einen [MarshalOptionsEnum](marshaloptionsenum.md)-Wert fest oder gibt den Wert zurück. Der Standardwert ist **adMarshalAll**.</span><span class="sxs-lookup"><span data-stu-id="e4646-p101">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value. The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4646-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e4646-108">Remarks</span></span>

<span data-ttu-id="e4646-p102">Bei der Verwendung eines clientseitigen [Recordsets](recordset-object-ado.md) werden Datensätze, die auf dem Client geändert wurden, wieder auf die mittlere Stufe bzw. den Webserver zurückgeschrieben. Das hierbei verwendete Verfahren wird Marshalling genannt. Dabei handelt es sich um das thread- oder prozessübergreifende Packen und Senden von Methodenparametern der Schnittstelle. Das Festlegen der **MarshalOptions** -Eigenschaft kann die Leistung verbessern, wenn geänderte Remotedaten zur Aktualisierung zurück auf die mittlere Stufe bzw. den Webserver gemarshallt werden.</span><span class="sxs-lookup"><span data-stu-id="e4646-p102">When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or Web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries. Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or Web server.</span></span>

<span data-ttu-id="e4646-111">**Remote Data Service-Verwendung** Diese Eigenschaft wird nur auf einem clientseitigen **Recordset-Objekt**verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4646-111">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>

