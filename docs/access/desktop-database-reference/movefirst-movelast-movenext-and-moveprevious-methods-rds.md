---
title: MoveFirst-, MoveLast-, MoveNext- und MovePrevious-Methoden (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fcef91204fd2390696911cd8a81e7fb232af2ae2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871437"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a><span data-ttu-id="ebea2-102">MoveFirst-, MoveLast-, MoveNext- und MovePrevious-Methoden (RDS)</span><span class="sxs-lookup"><span data-stu-id="ebea2-102">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)</span></span>


<span data-ttu-id="ebea2-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ebea2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ebea2-104">Wechselt zum ersten, letzten, nächsten oder vorherigen Datensatz in einem angegebenen [Recordset](recordset-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ebea2-104">Moves to the first, last, next, or previous record in a specified [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebea2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebea2-105">Syntax</span></span>

<span data-ttu-id="ebea2-106">*DataControl*. Recordset-Objekt. {</span><span class="sxs-lookup"><span data-stu-id="ebea2-106">*DataControl*.Recordset.{</span></span> <span data-ttu-id="ebea2-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span><span class="sxs-lookup"><span data-stu-id="ebea2-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span></span>

## <a name="parameters"></a><span data-ttu-id="ebea2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebea2-108">Parameters</span></span>

  - <span data-ttu-id="ebea2-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="ebea2-109">*DataControl*</span></span>

  - <span data-ttu-id="ebea2-110">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="ebea2-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebea2-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ebea2-111">Remarks</span></span>

<span data-ttu-id="ebea2-112">Sie können die **Move** -Methoden verwenden, mit der **RDS. DataControl** Objekt, das durch die Datensätze in der datengebundene Steuerelemente auf einer Webseite zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="ebea2-112">You can use the **Move** methods with the **RDS.DataControl** object to navigate through the data records in the data-bound controls on a webpage.</span></span> <span data-ttu-id="ebea2-113">Angenommen Sie, dass Sie ein **Recordset** in einem Raster durch Bindung an ein **RDS. anzeigen DataControl** Objekt.</span><span class="sxs-lookup"><span data-stu-id="ebea2-113">For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object.</span></span> <span data-ttu-id="ebea2-114">Sie können dann ersten, letzten, weiter und vorherige Schaltflächen, mit denen Benutzer, um diese Move zum ersten, letzten, nächsten klicken, einschließen oder vorherigen Datensatz im **Recordset**angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ebea2-114">You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**.</span></span> <span data-ttu-id="ebea2-115">Zu diesem Zweck Aufrufen der **Methoden MoveFirst**, **MoveLast**, **MoveNext**und **MovePrevious** -Methoden des der **RDS. DataControl** jeweils in den OnClick-Verfahren für die ersten, letzten, weiter und zurück-Tasten-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ebea2-115">You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively.</span></span> <span data-ttu-id="ebea2-116">Der [Adressbuch-Beispiel](address-book-navigation-buttons.md) zeigt, wie dazu.</span><span class="sxs-lookup"><span data-stu-id="ebea2-116">The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span></span>

