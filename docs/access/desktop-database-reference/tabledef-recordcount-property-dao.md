---
title: TableDef.RecordCount Property (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b1d1ab4fee16a9664733c71522cb07a49dde149
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474440"
---
# <a name="tabledefrecordcount-property-dao"></a>TableDef.RecordCount Property (DAO)


**Betrifft**: Access 2013 | Office 2013

Gibt die Gesamtzahl der Datensätze in einem **[TableDef](tabledef-object-dao.md)** -Objekt zurück. Schreibgeschützter **Long**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . RecordCount

*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die **RecordCount**-Eigenschaft eines **Recordset**- oder **TableDef**-Objekts ohne Datensätze hat den Wert 0.

Wenn Sie verknüpfte**TableDef**-Objekte verwenden, ist der Wert der **RecordCount**-Eigenschaft immer –1.

