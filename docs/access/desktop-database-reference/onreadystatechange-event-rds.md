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
# <a name="onreadystatechange-event-rds"></a>onReadyStateChange-Ereignis (RDS)

**Gilt für**: Access 2013, Office 2013

Das **onReadyStateChange**-Ereignis wird aufgerufen, wenn sich der Wert der [ReadyState](readystate-property-rds.md)-Eigenschaft ändert.

## <a name="syntax"></a>Syntax

onReadyStateChange

## <a name="parameters"></a>Parameter

Keine.

## <a name="remarks"></a>Bemerkungen

Die **ReadyState**-Eigenschaft zeigt den Fortschritt eines [RDS.DataControl](datacontrol-object-rds.md)-Objekts beim asynchronen Abrufen von Daten in sein [Recordset](recordset-object-ado.md)-Objekt an. Verwenden Sie das **onReadyStateChange**-Ereignis zur Überwachung der Änderungen der **ReadyState**-Eigenschaft, sobald diese auftreten. Dies ist effizienter als das regelmäßige Prüfen des Eigenschaftswerts.

