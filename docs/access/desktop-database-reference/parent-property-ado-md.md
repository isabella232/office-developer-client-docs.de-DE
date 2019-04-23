---
title: Parent-Eigenschaft (ADO MD)
TOCTitle: Parent property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0c0eef638cb76676cd2287a34c0e4b17bd89c4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287790"
---
# <a name="parent-property-ado-md"></a>Parent-Eigenschaft (ADO MD)


**Gilt für**: Access 2013, Office 2013

Gibt das Element an, das das übergeordnete Element des aktuellen Elements in einer Hierarchie ist.

## <a name="return-values"></a>Rückgabewerte

Gibt als Wert ein schreibgeschütztes [Member](member-object-ado-md.md)-Objekt zurück.

## <a name="remarks"></a>Bemerkungen

Ein Element auf der obersten Ebene einer Hierarchie (Wurzelebene) weist kein Hauptobjekt auf. Diese Eigenschaft wird nur für **Member**-Objekte unterstützt, die zu einem [Level](level-object-ado-md.md)-Objekt gehören. Wenn auf diese Eigenschaft durch **Member**-Objekte verwiesen wird, die zu einem [Position](position-object-ado-md.md)-Objekt gehören, tritt ein Fehler auf.

