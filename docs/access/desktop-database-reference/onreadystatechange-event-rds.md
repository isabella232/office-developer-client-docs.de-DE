---
title: onReadyStateChange-Ereignis (RDS)
TOCTitle: onReadyStateChange event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e52ef236a5e57efc965a6b3bd8ab6edd7533f2c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922209"
---
# <a name="onreadystatechange-event-rds"></a><span data-ttu-id="701e6-102">onReadyStateChange-Ereignis (RDS)</span><span class="sxs-lookup"><span data-stu-id="701e6-102">onReadyStateChange event (RDS)</span></span>


<span data-ttu-id="701e6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="701e6-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="701e6-104">Das **onReadyStateChange** -Ereignis wird aufgerufen, wenn sich der Wert der [ReadyState](readystate-property-rds.md)-Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="701e6-104">The **onReadyStateChange** event is called whenever the value of the [ReadyState](readystate-property-rds.md) property changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="701e6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="701e6-105">Syntax</span></span>

<span data-ttu-id="701e6-106">onReadyStateChange</span><span class="sxs-lookup"><span data-stu-id="701e6-106">onReadyStateChange</span></span>

## <a name="parameters"></a><span data-ttu-id="701e6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="701e6-107">Parameters</span></span>

<span data-ttu-id="701e6-108">Keine.</span><span class="sxs-lookup"><span data-stu-id="701e6-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="701e6-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="701e6-109">Remarks</span></span>

<span data-ttu-id="701e6-p101">Die **ReadyState** -Eigenschaft zeigt den Fortschritt eines [RDS.DataControl](datacontrol-object-rds.md)-Objekts beim asynchronen Abrufen von Daten in sein [Recordset](recordset-object-ado.md)-Objekt an. Verwenden Sie das **onReadyStateChange** -Ereignis zur Überwachung der Änderungen der **ReadyState** -Eigenschaft, sobald diese auftreten. Dies ist effizienter als das regelmäßige Prüfen des Eigenschaftswerts.</span><span class="sxs-lookup"><span data-stu-id="701e6-p101">The **ReadyState** property reflects the progress of an [RDS.DataControl](datacontrol-object-rds.md) object as it asynchronously retrieves data into its [Recordset](recordset-object-ado.md) object. Use the **onReadyStateChange** event to monitor changes in the **ReadyState** property whenever they occur. This is more efficient than periodically checking the property's value.</span></span>

