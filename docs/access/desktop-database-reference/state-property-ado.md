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
ms.localizationpriority: medium
ms.openlocfilehash: 311c21d628a77d3835ef40c849385e9946fd79dc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617398"
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

