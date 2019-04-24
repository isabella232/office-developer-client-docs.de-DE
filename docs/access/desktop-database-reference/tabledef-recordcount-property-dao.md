---
title: TableDef. RecordCount-Eigenschaft (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5eb9588927c9e35fea54964f16150735a7374cd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314287"
---
# <a name="tabledefrecordcount-property-dao"></a>TableDef. RecordCount-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt die Gesamtzahl der Datensätze in einem **[TableDef](tabledef-object-dao.md)** -Objekt zurück. Schreibgeschützter **Long**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . RecordCount

*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Ein **Recordset**- oder **TableDef**-Objekt ohne Datensätze hat eine **RecordCount**-Eigenschaftseinstellung von "0".

Wenn Sie verknüpfte**TableDef**-Objekte verwenden, ist der Wert der **RecordCount**-Eigenschaft immer –1.

