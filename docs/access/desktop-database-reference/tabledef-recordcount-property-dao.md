---
title: TableDef.RecordCount-Eigenschaft (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d73d4ce60757b7c9ca4758a6957dd9f176666757
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585179"
---
# <a name="tabledefrecordcount-property-dao"></a>TableDef.RecordCount-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt die Gesamtzahl der Datensätze in einem **[TableDef](tabledef-object-dao.md)** -Objekt zurück. Schreibgeschützter **Long**-Wert.

## <a name="syntax"></a>Syntax

*expression* .RecordCount

*Ausdruck* Eine Variable, die ein **TableDef**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Ein **Recordset**- oder **TableDef**-Objekt ohne Datensätze hat eine **RecordCount**-Eigenschaftseinstellung von "0".

Wenn Sie verknüpfte **TableDef**-Objekte verwenden, ist der Wert der **RecordCount**-Eigenschaft immer –1.

