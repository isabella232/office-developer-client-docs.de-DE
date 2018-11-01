---
title: Type-Eigenschaft (ADO MD)
TOCTitle: Type Property (ADO MD)
ms:assetid: 4aaa151e-1f02-aa7d-a9e5-e7019b200924
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249230(v=office.15)
ms:contentKeyID: 48544671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8f4a06956db9a051a130af0cbaa6f9090daa586b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889364"
---
# <a name="type-property-ado-md"></a>Type-Eigenschaft (ADO MD)


**Betrifft**: Access 2013, Office 2013

Gibt den Type des aktuellen Elements an.

## <a name="return-values"></a>Rückgabewerte

Gibt einen schreibgeschützten [MemberTypeEnum](membertypeenum.md)-Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird nur für [Member](member-object-ado-md.md)-Objekte unterstützt, die zu einem [Level](level-object-ado-md.md)-Objekt gehören. Wenn auf diese Eigenschaft durch **Member** -Objekte verwiesen wird, die zu einem [Position](position-object-ado-md.md)-Objekt gehören, tritt ein Fehler auf.

