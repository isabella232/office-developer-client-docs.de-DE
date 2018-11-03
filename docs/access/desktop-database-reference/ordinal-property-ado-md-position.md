---
title: Ordinal-Eigenschaft (ADO MD Position)
TOCTitle: Ordinal property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: abf355cc4d066604035fddbbe8f8a428d8c7a6b0
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944781"
---
# <a name="ordinal-property-ado-md-position"></a>Ordinal-Eigenschaft (ADO MD Position)


**Betrifft**: Access 2013, Office 2013

Identifiziert eindeutig eine Position auf einer Achse.

## <a name="return-values"></a>Rückgabewerte

Gibt einen schreibgeschützten, ganzzahligen **Long** -Wert zurück.

## <a name="remarks"></a>Hinweise

Die **Ordinal** -Eigenschaft eines [Position](position-object-ado-md.md)-Objekts entspricht dem Index des **Position** -Objekts innerhalb der [Positions](positions-collection-ado-md.md)-Auflistung.

Eine Zelle kann auf einfache Weise abgerufen werden, indem Sie die **Ordinal** -Eigenschaft des **Position** -Objekts entlang jeder Achse mit der [Item](item-property-ado-md-cellset.md)-Eigenschaft des [Cellset](cellset-object-ado-md.md)-Objekts verwenden.

