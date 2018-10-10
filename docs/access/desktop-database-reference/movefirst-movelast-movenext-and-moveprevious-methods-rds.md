---
title: MoveFirst-, MoveLast-, MoveNext- und MovePrevious-Methoden (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4671e57e3edb44bc1c927ca11f2cf79e70c2699
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474533"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a><span data-ttu-id="c19d9-102">MoveFirst-, MoveLast-, MoveNext- und MovePrevious-Methoden (RDS)</span><span class="sxs-lookup"><span data-stu-id="c19d9-102">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)</span></span>


<span data-ttu-id="c19d9-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c19d9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c19d9-104">Wechselt zum ersten, letzten, nächsten oder vorherigen Datensatz in einem angegebenen [Recordset](recordset-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c19d9-104">Moves to the first, last, next, or previous record in a specified [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c19d9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c19d9-105">Syntax</span></span>

<span data-ttu-id="c19d9-106">*DataControl*. Recordset-Objekt. {</span><span class="sxs-lookup"><span data-stu-id="c19d9-106">*DataControl*.Recordset.{</span></span> <span data-ttu-id="c19d9-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span><span class="sxs-lookup"><span data-stu-id="c19d9-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span></span>

## <a name="parameters"></a><span data-ttu-id="c19d9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c19d9-108">Parameters</span></span>

  - <span data-ttu-id="c19d9-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="c19d9-109">*DataControl*</span></span>

  - <span data-ttu-id="c19d9-110">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c19d9-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c19d9-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c19d9-111">Remarks</span></span>

<span data-ttu-id="c19d9-p102">Sie können die Move-Methoden für das RDS.DataControl-Objekt verwenden, um zwischen den Datensätzen in den datengebundenen Steuerelementen auf einer Webseite zu navigieren. Angenommen, Sie zeigen ein Recordset-Objekt durch Bindung an ein RDS.DataControl-Objekt in einem Raster an. Sie können anschließend die Schaltflächen Erster, Letzter, Nächster und Vorheriger einfügen, auf die die Benutzer klicken können, um zum ersten, letzten, nächsten oder vorherigen im Recordset-Objekt angezeigten Datensatz zu wechseln. Rufen Sie dazu in den onClick-Prozeduren die Methoden MoveFirst, MoveLast, MoveNext und MovePrevious des RDS.DataControl-Objekts für die Schaltflächen Erster, Letzter, Nächster bzw. Vorheriger auf. Die entsprechende Vorgehensweise wird im Beispiel zum Adressbuch erläutert.</span><span class="sxs-lookup"><span data-stu-id="c19d9-p102">You can use the **Move** methods with the **RDS.DataControl** object to navigate through the data records in the data-bound controls on a Web page. For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object. You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**. You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively. The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span></span>

