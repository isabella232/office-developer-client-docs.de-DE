---
title: Bestimmen, was unterstützt wird
TOCTitle: Determining what is supported
ms:assetid: 47b44dc9-e0fd-f204-0c68-e0de9247ee2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249221(v=office.15)
ms:contentKeyID: 48544602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 360a9e7a1f7dff51093216d0658cf72d74855b03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553095"
---
# <a name="determining-what-is-supported"></a>Bestimmen, was unterstützt wird

**Gilt für**: Access 2013, Office 2013

Mit der **Supports**-Methode bestimmen Sie, ob ein angegebenes **Recordset**-Objekt eine bestimmte Funktionalität unterstützt. Diese Methode weist die folgende Syntax auf:

`boolean = recordset.Supports( CursorOptions )`

**Supports** gibt einen booleschen Wert zurück, der anzeigt, ob alle vom Argument *CursorOptions* identifizierten Features vom Anbieter unterstützt werden. Mithilfe der **Supports**-Methode können Sie bestimmen, welche Funktionalität von einem **Recordset**-Objekt unterstützt wird. Falls das **Recordset**-Objekt die Features unterstützt, deren entsprechende Konstanten in *CursorOptions* vorhanden sind, gibt die **Supports**-Methode **True** zurück. Andernfalls wird **False** zurückgegeben.

Mithilfe der **Supports** -Methode können Sie überprüfen, ob Sie mit dem **Recordset** -Objekt neue Datensätze hinzufügen, Lesezeichen verwenden, die **Find** -Methode verwenden, den Fensterinhalt verschieben, die **Index** -Eigenschaft verwenden und Batchaktualisierungen ausführen können. Eine vollständige Liste der Konstanten und deren Bedeutung finden Sie unter [CursorOptionEnum](cursoroptionenum.md).

Die **Supports** -Methode kann zwar **True** für eine bestimmte Funktionalität zurückgeben, aber dies garantiert nicht, dass der Anbieter das Feature unter allen Umständen zur Verfügung stellen kann. Die **Supports** -Methode gibt einfach zurück, ob der Anbieter die angegebene Funktionalität unterstützen kann, vorausgesetzt bestimmte Bedingungen sind erfüllt. Beispielsweise kann die **Supports** -Methode angeben, dass ein **Recordset** -Objekt Aktualisierungen unterstützt, obwohl der Cursor auf einer Verknüpfung mehrerer Tabellen basiert , von denen manche Spalten nicht aktualisierbar sind.

