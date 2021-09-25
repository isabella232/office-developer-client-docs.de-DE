---
title: Ordinal-Eigenschaft (ADO MD Position)
TOCTitle: Ordinal property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c82565fec9dea3b985185dfc198861caca9cbe6f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593915"
---
# <a name="ordinal-property-ado-md-position"></a>Ordinal-Eigenschaft (ADO MD Position)


**Gilt für**: Access 2013, Office 2013

Identifiziert eindeutig eine Position auf einer Achse.

## <a name="return-values"></a>Rückgabewerte

Gibt einen schreibgeschützten, ganzzahligen **Long**-Wert zurück.

## <a name="remarks"></a>HinwBemerkungeneise

Die **Ordinal**-Eigenschaft eines [Position](position-object-ado-md.md)-Objekts entspricht dem Index des **Position**-Objekts innerhalb der [Positions](positions-collection-ado-md.md)-Auflistung.

Eine Zelle kann auf einfache Weise abgerufen werden, indem Sie die **Ordinal**-Eigenschaft des **Position**-Objekts entlang jeder Achse mit der [Item](item-property-ado-md-cellset.md)-Eigenschaft des [Cellset](cellset-object-ado-md.md)-Objekts verwenden.

