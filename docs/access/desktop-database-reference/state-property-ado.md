---
title: State-Eigenschaft (ADO)
TOCTitle: State property (ADO)
ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15)
ms:contentKeyID: 48547053
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231176
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0bce3f87a6530315a128396fe0e4de5390e0f47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308533"
---
# <a name="state-property-ado"></a>State-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Für alle entsprechenden Objekte wird angegeben, ob der Status des Objekts open oder closed entspricht.

Für alle entsprechenden Objekte, durch die eine asynchrone Methode ausgeführt wird, wird angegeben, ob der aktuelle Status des Objekts connecting, executing oder retrieving entspricht.

## <a name="return-value"></a>Rückgabewert

Gibt einen **Long** -Wert zurück, bei dem es sich um einen [ObjectStateEnum](objectstateenum.md)-Wert handeln kann. Der Standardwert ist **adStateClosed**.

## <a name="remarks"></a>Bemerkungen

Mit der **State**-Eigenschaft können Sie jederzeit den aktuellen Status eines bestimmten Objekts ermitteln.

Die **State** -Eigenschaft des Objekts kann kombinierte Werte besitzen. Wenn beispielsweise eine Anweisung ausgeführt wird, besitzt die Eigenschaft einen aus **adStateOpen** und **adStateExecuting** bestehenden kombinierten Wert.

Die **State** -Eigenschaft ist schreibgeschützt.

