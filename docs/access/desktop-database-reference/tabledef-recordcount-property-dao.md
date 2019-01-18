---
title: TableDef.RecordCount-Eigenschaft (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5eb9588927c9e35fea54964f16150735a7374cd5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722865"
---
# <a name="tabledefrecordcount-property-dao"></a>TableDef.RecordCount-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Gibt die Gesamtzahl der Datensätze in einem **[TableDef](tabledef-object-dao.md)** -Objekt zurück. Schreibgeschützter **Long**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . RecordCount

*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die **RecordCount**-Eigenschaft eines **Recordset**- oder **TableDef**-Objekts ohne Datensätze hat den Wert 0.

Wenn Sie verknüpfte**TableDef**-Objekte verwenden, ist der Wert der **RecordCount**-Eigenschaft immer –1.

