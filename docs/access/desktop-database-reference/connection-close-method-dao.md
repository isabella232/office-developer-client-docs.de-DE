---
title: Connection.Close durchführen-Methode (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b6f84b9580fbd6256069de57b2295cf3460edaf8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928978"
---
# <a name="connectionclose-method-dao"></a><span data-ttu-id="a88ec-102">Connection.Close durchführen-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="a88ec-102">Connection.Close method (DAO)</span></span>


<span data-ttu-id="a88ec-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a88ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a88ec-104">Schließt ein geöffnetes **Connection**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a88ec-104">Closes an open **Connection**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a88ec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a88ec-105">Syntax</span></span>

<span data-ttu-id="a88ec-106">*Ausdruck* . Schließen Sie</span><span class="sxs-lookup"><span data-stu-id="a88ec-106">*expression* .Close</span></span>

<span data-ttu-id="a88ec-107">*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="a88ec-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a88ec-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a88ec-108">Remarks</span></span>

<span data-ttu-id="a88ec-109">Ist das **Recordset** -Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="a88ec-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="a88ec-p101">Wenn Sie versuchen, ein **Connection** -Objekt zu schließen, für das noch **Recordset** -Objekte geöffnet sind, werden die **Recordset** -Objekte geschlossen, und alle ausstehenden Aktualisierungen oder Bearbeitungen werden abgebrochen. Auch wenn Sie versuchen, ein **Workspace** -Objekt zu schließen, für das noch **Connection** -Objekte geöffnet sind, werden diese **Connection** -Objekte geschlossen. Daraufhin werden deren **Recordset** -Objekte ebenfalls geschlossen.</span><span class="sxs-lookup"><span data-stu-id="a88ec-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="a88ec-112">Eine Alternative für die **Close** -Methode den Wert einer Objektvariable auf **Nothing** festgelegt ist (Set DbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="a88ec-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

