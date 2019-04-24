---
title: DrilledDown-Eigenschaft (ADO MD)
TOCTitle: DrilledDown property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40a97c7f755f681169c77c3a2077ee41d9cdc980
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293686"
---
# <a name="drilleddown-property-ado-md"></a>DrilledDown-Eigenschaft (ADO MD)


**Gilt für**: Access 2013, Office 2013

Gibt an, ob dem Element auf der Achse direkt untergeordnete Elemente folgen.

## <a name="return-values"></a>Rückgabewerte

Gibt einen schreibgeschützten **Boolean** -Wert zurück. **DrilledDown** gibt **True** zurück, wenn sich keine untergeordneten Elemente des aktuellen Elements auf der Achse befinden. **DrilledDown** gibt **False** zurück, wenn sich ein oder mehrere untergeordnete Elemente des aktuellen Elements auf der Achse befinden.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **DrilledDown** -Eigenschaft, um zu bestimmen, ob sich mindestens ein untergeordnetes Element in direkter Folge des aktuellen Elements auf der Achse befindet. Diese Information ist beim Anzeigen des Elements nützlich.

Diese Eigenschaft wird nur für [Member](member-object-ado-md.md)-Objekte unterstützt, die zu einem [Position](position-object-ado-md.md)-Objekt gehören. Wenn auf diese Eigenschaft durch **Member** -Objekte verwiesen wird, die zu einem [Level](level-object-ado-md.md)-Objekt gehören, tritt ein Fehler auf.

