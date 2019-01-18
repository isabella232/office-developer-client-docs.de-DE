---
title: Recordset.Close-Methode (DAO)
TOCTitle: Close Method
ms:assetid: e76a81c6-ca0d-e310-c1dc-cbc5d6f6248b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836011(v=office.15)
ms:contentKeyID: 48548404
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f7cbd94bfacc91bfe080d33807ca7989c1dca661
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717454"
---
# <a name="recordsetclose-method-dao"></a><span data-ttu-id="153cb-102">Recordset.Close-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="153cb-102">Recordset.Close method (DAO)</span></span>


<span data-ttu-id="153cb-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="153cb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="153cb-104">Schließt ein geöffnetes **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="153cb-104">Closes an open **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="153cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="153cb-105">Syntax</span></span>

<span data-ttu-id="153cb-106">*Ausdruck* . Schließen Sie</span><span class="sxs-lookup"><span data-stu-id="153cb-106">*expression* .Close</span></span>

<span data-ttu-id="153cb-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="153cb-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="153cb-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="153cb-108">Remarks</span></span>

<span data-ttu-id="153cb-109">Ist das **Recordset** -Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="153cb-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="153cb-p101">Wenn Sie versuchen, ein **Connection** -Objekt zu schließen, für das noch **Recordset** -Objekte geöffnet sind, werden die **Recordset** -Objekte geschlossen, und alle ausstehenden Aktualisierungen oder Bearbeitungen werden abgebrochen. Auch wenn Sie versuchen, ein **Workspace** -Objekt zu schließen, für das noch **Connection** -Objekte geöffnet sind, werden diese **Connection** -Objekte geschlossen. Daraufhin werden deren **Recordset** -Objekte ebenfalls geschlossen.</span><span class="sxs-lookup"><span data-stu-id="153cb-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="153cb-112">Eine Alternative für die **Close** -Methode den Wert einer Objektvariable auf **Nothing** festgelegt ist (Set DbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="153cb-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

