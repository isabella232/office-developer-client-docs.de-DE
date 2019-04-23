---
title: onReadyStateChange-Ereignis (RDS)
TOCTitle: onReadyStateChange event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ec2104634d9158d59d488b50d543cf0e57d9bd62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288490"
---
# <a name="onreadystatechange-event-rds"></a><span data-ttu-id="28d32-102">onReadyStateChange-Ereignis (RDS)</span><span class="sxs-lookup"><span data-stu-id="28d32-102">onReadyStateChange event (RDS)</span></span>

<span data-ttu-id="28d32-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28d32-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28d32-104">Das **onReadyStateChange**-Ereignis wird aufgerufen, wenn sich der Wert der [ReadyState](readystate-property-rds.md)-Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="28d32-104">The **onReadyStateChange** event is called whenever the value of the [ReadyState](readystate-property-rds.md) property changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="28d32-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="28d32-105">Syntax</span></span>

<span data-ttu-id="28d32-106">onReadyStateChange</span><span class="sxs-lookup"><span data-stu-id="28d32-106">onReadyStateChange</span></span>

## <a name="parameters"></a><span data-ttu-id="28d32-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="28d32-107">Parameters</span></span>

<span data-ttu-id="28d32-108">Keine.</span><span class="sxs-lookup"><span data-stu-id="28d32-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="28d32-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28d32-109">Remarks</span></span>

<span data-ttu-id="28d32-p101">Die **ReadyState**-Eigenschaft zeigt den Fortschritt eines [RDS.DataControl](datacontrol-object-rds.md)-Objekts beim asynchronen Abrufen von Daten in sein [Recordset](recordset-object-ado.md)-Objekt an. Verwenden Sie das **onReadyStateChange**-Ereignis zur Überwachung der Änderungen der **ReadyState**-Eigenschaft, sobald diese auftreten. Dies ist effizienter als das regelmäßige Prüfen des Eigenschaftswerts.</span><span class="sxs-lookup"><span data-stu-id="28d32-p101">The **ReadyState** property reflects the progress of an [RDS.DataControl](datacontrol-object-rds.md) object as it asynchronously retrieves data into its [Recordset](recordset-object-ado.md) object. Use the **onReadyStateChange** event to monitor changes in the **ReadyState** property whenever they occur. This is more efficient than periodically checking the property's value.</span></span>

