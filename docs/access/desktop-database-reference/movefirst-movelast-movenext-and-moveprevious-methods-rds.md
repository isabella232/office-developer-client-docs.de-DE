---
title: MoveFirst-, MoveLast-, MoveNext-und MovePrevious-Methoden (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5631ce68a0479146e15ba74b41af5669d86175a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288686"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a><span data-ttu-id="1bd23-102">MoveFirst-, MoveLast-, MoveNext-und MovePrevious-Methoden (RDS)</span><span class="sxs-lookup"><span data-stu-id="1bd23-102">MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)</span></span>

<span data-ttu-id="1bd23-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1bd23-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1bd23-104">Wechselt zum ersten, letzten, nächsten oder vorherigen Datensatz in einem angegebenen [Recordset](recordset-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1bd23-104">Moves to the first, last, next, or previous record in a specified [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bd23-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bd23-105">Syntax</span></span>

<span data-ttu-id="1bd23-106">*DataControl*. Recordset. {</span><span class="sxs-lookup"><span data-stu-id="1bd23-106">*DataControl*.Recordset.{</span></span> <span data-ttu-id="1bd23-107">MoveFirst | MoveLast | MoveNext | MovePrevious</span><span class="sxs-lookup"><span data-stu-id="1bd23-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span></span>

## <a name="parameters"></a><span data-ttu-id="1bd23-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bd23-108">Parameters</span></span>

|<span data-ttu-id="1bd23-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bd23-109">Parameter</span></span>|<span data-ttu-id="1bd23-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1bd23-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1bd23-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="1bd23-111">*DataControl*</span></span> |<span data-ttu-id="1bd23-112">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="1bd23-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1bd23-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1bd23-113">Remarks</span></span>

<span data-ttu-id="1bd23-114">Sie können die **Move** -Methoden mit **RDS verwenden. DataControl** -Objekt, um durch die Datensätze in den datengebundenen Steuerelementen auf einer Webseite zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="1bd23-114">You can use the **Move** methods with the **RDS.DataControl** object to navigate through the data records in the data-bound controls on a webpage.</span></span> 

<span data-ttu-id="1bd23-115">For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object.</span><span class="sxs-lookup"><span data-stu-id="1bd23-115">For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object.</span></span> <span data-ttu-id="1bd23-116">You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="1bd23-116">You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**.</span></span> <span data-ttu-id="1bd23-117">You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively.</span><span class="sxs-lookup"><span data-stu-id="1bd23-117">You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively.</span></span> <span data-ttu-id="1bd23-118">The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span><span class="sxs-lookup"><span data-stu-id="1bd23-118">The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span></span>

