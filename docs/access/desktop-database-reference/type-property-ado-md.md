---
title: Type-Eigenschaft (ADO MD)
TOCTitle: Type property (ADO MD)
ms:assetid: 4aaa151e-1f02-aa7d-a9e5-e7019b200924
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249230(v=office.15)
ms:contentKeyID: 48544671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1c7b361a41fedc234d95d87a3002713bc3cf9853
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588917"
---
# <a name="type-property-ado-md"></a>Type-Eigenschaft (ADO MD)


**Gilt für**: Access 2013, Office 2013

Gibt den Type des aktuellen Elements an.

## <a name="return-values"></a>Rückgabewerte

Gibt einen schreibgeschützten [MemberTypeEnum](membertypeenum.md)-Wert zurück.

## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird nur für [Member](member-object-ado-md.md)-Objekte unterstützt, die zu einem [Level](level-object-ado-md.md)-Objekt gehören. Wenn auf diese Eigenschaft durch **Member**-Objekte verwiesen wird, die zu einem [Position](position-object-ado-md.md)-Objekt gehören, tritt ein Fehler auf.

