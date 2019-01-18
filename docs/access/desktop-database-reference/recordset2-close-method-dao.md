---
title: Recordset2.Close-Methode (DAO)
TOCTitle: Close Method
ms:assetid: ef816969-9857-37cf-9562-d5c80d2815ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836412(v=office.15)
ms:contentKeyID: 48548584
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 178dec604a185da94493e6d586249bd2a633899c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708431"
---
# <a name="recordset2close-method-dao"></a><span data-ttu-id="dffdc-102">Recordset2.Close-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="dffdc-102">Recordset2.Close method (DAO)</span></span>


<span data-ttu-id="dffdc-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dffdc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dffdc-104">Schließt ein geöffnetes **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="dffdc-104">Closes an open **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="dffdc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dffdc-105">Syntax</span></span>

<span data-ttu-id="dffdc-106">*Ausdruck* . Schließen Sie</span><span class="sxs-lookup"><span data-stu-id="dffdc-106">*expression* .Close</span></span>

<span data-ttu-id="dffdc-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="dffdc-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dffdc-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dffdc-108">Remarks</span></span>

<span data-ttu-id="dffdc-109">Ist das **Recordset** -Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="dffdc-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="dffdc-p101">Wenn Sie versuchen, ein **Connection** -Objekt zu schließen, für das noch **Recordset** -Objekte geöffnet sind, werden die **Recordset** -Objekte geschlossen, und alle ausstehenden Aktualisierungen oder Bearbeitungen werden abgebrochen. Auch wenn Sie versuchen, ein **Workspace** -Objekt zu schließen, für das noch **Connection** -Objekte geöffnet sind, werden diese **Connection** -Objekte geschlossen. Daraufhin werden deren **Recordset** -Objekte ebenfalls geschlossen.</span><span class="sxs-lookup"><span data-stu-id="dffdc-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="dffdc-112">Eine Alternative für die **Close** -Methode den Wert einer Objektvariable auf **Nothing** festgelegt ist (Set DbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="dffdc-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

