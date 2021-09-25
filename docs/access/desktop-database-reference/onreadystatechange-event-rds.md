---
title: onReadyStateChange-Ereignis (RDS)
TOCTitle: onReadyStateChange event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 81e3baa586b428c28e90de68c4632a3b28e5a699
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568803"
---
# <a name="onreadystatechange-event-rds"></a>onReadyStateChange-Ereignis (RDS)

**Gilt für**: Access 2013, Office 2013

Das **onReadyStateChange**-Ereignis wird aufgerufen, wenn sich der Wert der [ReadyState](readystate-property-rds.md)-Eigenschaft ändert.

## <a name="syntax"></a>Syntax

onReadyStateChange

## <a name="parameters"></a>Parameter

Keine.

## <a name="remarks"></a>HinwBemerkungeneise

Die **ReadyState**-Eigenschaft zeigt den Fortschritt eines [RDS.DataControl](datacontrol-object-rds.md)-Objekts beim asynchronen Abrufen von Daten in sein [Recordset](recordset-object-ado.md)-Objekt an. Verwenden Sie das **onReadyStateChange**-Ereignis zur Überwachung der Änderungen der **ReadyState**-Eigenschaft, sobald diese auftreten. Dies ist effizienter als das regelmäßige Prüfen des Eigenschaftswerts.

