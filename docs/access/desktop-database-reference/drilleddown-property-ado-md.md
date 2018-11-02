---
title: DrilledDown-Eigenschaft (ADO MD)
TOCTitle: DrilledDown property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9d521176eeb2ac2e83ef05d05d3572dfba543812
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931001"
---
# <a name="drilleddown-property-ado-md"></a>DrilledDown-Eigenschaft (ADO MD)


**Betrifft**: Access 2013, Office 2013

Gibt an, ob dem Element auf der Achse direkt untergeordnete Elemente folgen.

## <a name="return-values"></a>Rückgabewerte

Gibt einen schreibgeschützten **Boolean** -Wert zurück. **DrilledDown** gibt **True** zurück, wenn sich keine untergeordneten Elemente des aktuellen Elements auf der Achse befinden. **DrilledDown** gibt **False** zurück, wenn sich ein oder mehrere untergeordnete Elemente des aktuellen Elements auf der Achse befinden.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **DrilledDown** -Eigenschaft, um zu bestimmen, ob sich mindestens ein untergeordnetes Element in direkter Folge des aktuellen Elements auf der Achse befindet. Diese Information ist beim Anzeigen des Elements nützlich.

Diese Eigenschaft wird nur für [Member](member-object-ado-md.md)-Objekte unterstützt, die zu einem [Position](position-object-ado-md.md)-Objekt gehören. Wenn auf diese Eigenschaft durch **Member** -Objekte verwiesen wird, die zu einem [Level](level-object-ado-md.md)-Objekt gehören, tritt ein Fehler auf.

