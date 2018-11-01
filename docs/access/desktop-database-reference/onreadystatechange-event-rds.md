---
title: onReadyStateChange-Ereignis (RDS)
TOCTitle: onReadyStateChange Event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7bea7d7ae5a7fe0681af315c8569bf9b67d8bd82
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869232"
---
# <a name="onreadystatechange-event-rds"></a>onReadyStateChange-Ereignis (RDS)


**Betrifft**: Access 2013, Office 2013


Das **onReadyStateChange** -Ereignis wird aufgerufen, wenn sich der Wert der [ReadyState](readystate-property-rds.md)-Eigenschaft ändert.

## <a name="syntax"></a>Syntax

onReadyStateChange

## <a name="parameters"></a>Parameter

Keine.

## <a name="remarks"></a>Hinweise

Die **ReadyState** -Eigenschaft zeigt den Fortschritt eines [RDS.DataControl](datacontrol-object-rds.md)-Objekts beim asynchronen Abrufen von Daten in sein [Recordset](recordset-object-ado.md)-Objekt an. Verwenden Sie das **onReadyStateChange** -Ereignis zur Überwachung der Änderungen der **ReadyState** -Eigenschaft, sobald diese auftreten. Dies ist effizienter als das regelmäßige Prüfen des Eigenschaftswerts.

