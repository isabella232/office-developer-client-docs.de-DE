---
title: Ordinal-Eigenschaft (ADO MD Cell)
TOCTitle: Ordinal property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 91b8d66929e360f88385b6773a03fcaffb79161d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717412"
---
# <a name="ordinal-property-ado-md-cell"></a>Ordinal-Eigenschaft (ADO MD Cell)


**Betrifft**: Access 2013, Office 2013

Identifiziert eine Zelle eindeutig durch ihre Position innerhalb einer Zellmenge.

## <a name="return-values"></a>Rückgabewerte

Gibt einen schreibgeschützten, ganzzahligen **Long** -Wert zurück.

## <a name="remarks"></a>Hinweise

Durch den Ordnungswert einer Zelle wird die Zelle innerhalb einer Zellmenge eindeutig identifiziert. Bei diesem Konzept sind die Zellen in einer Zellmenge nummeriert, als wäre die Zellmenge ein *p*-dimensionales Array, wobei *p* die Anzahl der [Achsen](axes-collection-ado-md.md) darstellt. Zellen sind zeilenweise nummeriert (beginnend bei 0).

Der Ordnungswert der Zelle kann mit der [Item](item-property-ado-md-cellset.md)-Eigenschaft des [Cellset](cellset-object-ado-md.md)-Objekts verwendet werden, um die [Zelle](cell-object-ado-md.md) schnell abzurufen.

