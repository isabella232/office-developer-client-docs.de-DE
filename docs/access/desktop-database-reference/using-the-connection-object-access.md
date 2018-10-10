---
title: Using the Connection Object (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cd3e691258fe5950f40c36a1efcaed8e79810c7a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473845"
---
# <a name="using-the-connection-object-access"></a>Using the Connection Object (Access)


**Betrifft**: Access 2013 | Office 2013

Ein **Connection** -Objekt stellt eine eindeutige Sitzung mit einer Datenquelle dar. Bei einem Client-/Server-Datenbanksystem kann es einer tatsächlichen Netzwerkverbindung mit dem Server entsprechen. In Abhängigkeit von der vom Anbieter unterstützten Funktionalität können bestimmte Auflistungen, Methoden oder Eigenschaften eines **Connection** -Objekts nicht verfügbar sein.

Vor dem Öffnen eines **Connection** -Objekts müssen Sie bestimmte Informationen zur Datenquelle und zum Verbindungstyp definieren. Der Parameter *ConnectionString* der **Open** -Methode des **Connection** -Objekts – oder der **ConnectionString** -Eigenschaft auf das **Connection** -Objekt – in der Regel enthält die meisten dieser Informationen. Eine Verbindungszeichenfolge ist eine Abfolge von Buchstaben, mit der eine variable Anzahl von Argumenten definiert wird. Die Argumente - einige sind für ADO erforderlich, andere wiederum anbieterspezifisch - enthalten Informationen, die das **Connection** -Objekt zum Ausführen seiner Aufgaben benötigt. Die Argumente, die der *ConnectionString* -Parameter bilden werden mit Semikolons (;) voneinander getrennt.


> [!NOTE]
> <P>Sie können auch eine ODBC-Datenquellennamen (DSN) oder eine Datei Daten Link (UDL) in eine Verbindungszeichenfolge angeben. Weitere Informationen zu dem DSNs finden Sie unter Datenquellen in Teil 1 von der <EM>ODBC-Programmer's Reference</EM>. Weitere Informationen zu UDLs finden Sie unter Data Link API Overview in der <EM>OLE DB Programmer's Reference</EM>.</P>


