---
title: QueryDefs.Count-Eigenschaft (DAO)
TOCTitle: Count Property
ms:assetid: 8caa01c5-692f-95e4-4b11-6e6c591f5872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197340(v=office.15)
ms:contentKeyID: 48546240
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95624c82ee9ab322eec5455759cf4ec2e9708dba
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707430"
---
# <a name="querydefscount-property-dao"></a>QueryDefs.Count-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Gibt die Anzahl der Objekte in der angegebenen Auflistung zurück. Schreibgeschützt.

## <a name="syntax"></a>Syntax

*Ausdruck* . Count

*Ausdruck* Eine Variable, die ein **QueryDefs** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Da die Elemente einer Auflistung mit 0 beginnen, müssen Schleifen immer mit dem Element 0 starten und mit dem Wert der **Count**-Eigenschaft minus 1 enden. Wenn eine Schleife die Elemente einer Auflistung durchsucht, ohne die **Count**-Eigenschaft zu überprüfen, können Sie einen **For Each...Next**-Befehl verwenden.

Der Wert der **Count**-Eigenschaft ist nie Null. Wenn ihr Wert 0 ist, sind keine Objekte in der Auflistung enthalten.

