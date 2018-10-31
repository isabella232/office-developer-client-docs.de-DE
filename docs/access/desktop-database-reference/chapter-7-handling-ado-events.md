---
title: 'Kapitel 7: Behandeln von ADO-Ereignissen'
TOCTitle: 'Chapter 7: Handling ADO Events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 816dd98e5e4c21f3159edf18b5687b2b0578e399
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860840"
---
# <a name="chapter-7-handling-ado-events"></a>Kapitel 7: Behandeln von ADO-Ereignissen


**Betrifft**: Access 2013 | Office 2013

Das ADO-Ereignismodell unterstützt bestimmte synchrone und asynchrone ADO-Operationen, durch die *Ereignisse* oder Benachrichtigungen ausgegeben werden, bevor die Operation gestartet wird oder nachdem sie abgeschlossen ist. Ein Ereignis ist tatsächlich ein Aufruf an eine Ereignishandlerroutine, die Sie in der Anwendung definieren.

Wenn Sie Handlerfunktionen oder -prozeduren für die Gruppe der vor dem Starten der Operation auftretenden Ereignisse bereitstellen, können Sie die an die Operation übergebenen Parameter überprüfen. Da die Operation noch nicht ausgeführt wurde, können Sie sie abbrechen oder zulassen, dass sie abgeschlossen wird.

Die Gruppe der nach Abschluss einer Operation auftretenden Ereignisse ist besonders wichtig, wenn Sie ADO asynchron verwenden. Beispielsweise wird eine Anwendung, durch die eine asynchrone Recordset.Open-Operation gestartet wird, von einem ExecuteComplete-Ereignis benachrichtigt, wenn die Operation abgeschlossen ist.

Durch das Verwenden des ADO-Ereignismodells entsteht mehr Aufwand für die Anwendung, jedoch wird auch erheblich mehr Flexibilität bereitgestellt als bei anderen Methoden für den Umgang mit asynchronen Operationen, z. B. beim Überwachen der [State](state-property-ado.md)-Eigenschaft eines Objekts mit einer Schleife.

In diesem Kapitel werden die folgenden Themen behandelt:

- [ADO-Ereignishandler (Zusammenfassung)](ado-event-handler-summary.md)

- [Arten von Ereignissen](types-of-events.md)

- [Ereignisparameter](event-parameters.md)

- [Zusammenspiel von Ereignishandlern](how-event-handlers-work-together.md)

- [ADO Event Instantiation by Language (ADO)](ado-event-instantiation-by-language-ado.md)