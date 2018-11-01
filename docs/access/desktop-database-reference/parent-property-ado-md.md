---
title: Parent-Eigenschaft (ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7beba341a2374e1868c67c8f7b4fab73c71c0ba8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880299"
---
# <a name="parent-property-ado-md"></a>Parent-Eigenschaft (ADO MD)


**Betrifft**: Access 2013, Office 2013

Gibt das Element an, das das übergeordnete Element des aktuellen Elements in einer Hierarchie ist.

## <a name="return-values"></a>Rückgabewerte

Gibt als Wert ein schreibgeschütztes [Member](member-object-ado-md.md)-Objekt zurück.

## <a name="remarks"></a>Hinweise

Ein Element auf der obersten Ebene einer Hierarchie (Wurzelebene) weist kein Hauptobjekt auf. Diese Eigenschaft wird nur für **Member** -Objekte unterstützt, die zu einem [Level](level-object-ado-md.md)-Objekt gehören. Wenn auf diese Eigenschaft durch **Member** -Objekte verwiesen wird, die zu einem [Position](position-object-ado-md.md)-Objekt gehören, tritt ein Fehler auf.

