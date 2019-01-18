---
title: IsolationLevel-Eigenschaft (ADO)
TOCTitle: IsolationLevel property (ADO)
ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15)
ms:contentKeyID: 48543493
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4eb46fa97b831030617916d03557b5bf9af9606d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698869"
---
# <a name="isolationlevel-property-ado"></a><span data-ttu-id="dc06e-102">IsolationLevel-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="dc06e-102">IsolationLevel property (ADO)</span></span>


<span data-ttu-id="dc06e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc06e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc06e-104">Gibt die Isolationsstufe für ein [Connection](connection-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="dc06e-104">Indicates the level of isolation for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="dc06e-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dc06e-105">Settings and return values</span></span>

<span data-ttu-id="dc06e-p101">Legt einen [IsolationLevelEnum](isolationlevelenum.md)-Wert fest oder gibt den Wert zurück. Der Standardwert ist **AdXactChaos**.</span><span class="sxs-lookup"><span data-stu-id="dc06e-p101">Sets or returns an [IsolationLevelEnum](isolationlevelenum.md) value. The default is **adXactChaos**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc06e-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dc06e-108">Remarks</span></span>

<span data-ttu-id="dc06e-p102">Legen Sie mit der **IsolationLevel** -Eigenschaft die Isolationsstufe eines **Connection** -Objekts fest. Die Einstellung wird erst beim nächsten Aufrufen der [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Methode wirksam. Wenn die von Ihnen angeforderte Isolationsstufe nicht verfügbar ist, gibt der Anbieter möglicherweise die nächsthöhere Isolationsstufe zurück.</span><span class="sxs-lookup"><span data-stu-id="dc06e-p102">Use the **IsolationLevel** property to set the isolation level of a **Connection** object. The setting does not take effect until the next time you call the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method. If the level of isolation you request is unavailable, the provider may return the next greater level of isolation.</span></span>

<span data-ttu-id="dc06e-112">Die **IsolationLevel** -Eigenschaft ist nicht schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="dc06e-112">The **IsolationLevel** property is read/write.</span></span>

<span data-ttu-id="dc06e-113">**Remote Data Service-Verwendung** Wenn für ein clientseitiges Connection-Objekt verwendet wird, kann die **IsolationLevel** -Eigenschaft nur auf **AdXactUnspecified**festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dc06e-113">**Remote Data Service Usage**When used on a client-side Connection object, the **IsolationLevel** property can be set only to **adXactUnspecified**.</span></span>

<span data-ttu-id="dc06e-p103">Da Benutzer mit nicht verbundenen **Recordset** -Objekten in einem clientbasierten Cache arbeiten, können Probleme mit mehreren Benutzern auftreten. Wenn beispielsweise zwei unterschiedliche Benutzer versuchen, denselben Datensatz zu aktualisieren, hat der Benutzer Erfolg, der den Datensatz zuerst aktualisiert. Die Aktualisierungsanforderung des zweiten Benutzers verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="dc06e-p103">Because users are working with disconnected **Recordset** objects on a client-side cache, there may be multiuser issues. For instance, when two different users try to update the same record, Remote Data Service simply allows the user who updates the record first to "win." The second user's update request will fail with an error.</span></span>

