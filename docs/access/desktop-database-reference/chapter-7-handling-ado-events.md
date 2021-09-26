---
title: 'Kapitel 7: Behandeln von ADO-Ereignissen'
TOCTitle: 'Chapter 7: Handling ADO events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e5cd1d46441cb073d1b5a9b5361c8ea3bac15aa8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627086"
---
# <a name="chapter-7-handling-ado-events"></a>Kapitel 7: Behandeln von ADO-Ereignissen

**Gilt für**: Access 2013, Office 2013

Das ADO-Ereignismodell unterstützt bestimmte synchrone und asynchrone ADO-Operationen, durch die *Ereignisse* oder Benachrichtigungen ausgegeben werden, bevor die Operation gestartet wird oder nachdem sie abgeschlossen ist. Ein Ereignis ist tatsächlich ein Aufruf an eine Ereignishandlerroutine, die Sie in der Anwendung definieren.

Wenn Sie Handlerfunktionen oder -prozeduren für die Gruppe der vor dem Starten der Operation auftretenden Ereignisse bereitstellen, können Sie die an die Operation übergebenen Parameter überprüfen. Da die Operation noch nicht ausgeführt wurde, können Sie sie abbrechen oder zulassen, dass sie abgeschlossen wird.

The group of events that occur after an operation completes are especially important if you use ADO asynchronously. For example, an application that starts an asynchronous [Recordset.Open](open-method-ado-recordset.md) operation is notified by an execution complete event when the operation concludes.

Durch das Verwenden des ADO-Ereignismodells entsteht mehr Aufwand für die Anwendung, jedoch wird auch erheblich mehr Flexibilität bereitgestellt als bei anderen Methoden für den Umgang mit asynchronen Operationen, z. B. beim Überwachen der [State](state-property-ado.md)-Eigenschaft eines Objekts mit einer Schleife.

In diesem Kapitel werden die folgenden Themen behandelt:

- [Zusammenfassung über den ADO-Ereignishandler](ado-event-handler-summary.md)
- [Typen von Ereignissen](types-of-events.md)
- [Ereignisparameter](event-parameters.md)
- [Zusammenspiel von Ereignishandlern](how-event-handlers-work-together.md)
- [ADO-Ereignisinstanziierung nach Sprache (ADO)](ado-event-instantiation-by-language-ado.md)
