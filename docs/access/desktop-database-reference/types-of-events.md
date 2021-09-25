---
title: Ereignistypen (Access-Desktopdatenbankreferenz)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 23b4b794b72e06695b633cb6b2dc4540b3aa0356
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562146"
---
# <a name="types-of-events"></a>Typen von Ereignissen


**Gilt für**: Access 2013, Office 2013



There are two basic types of events. "Will Events," which are called before an operation starts, usually include "Will" in their names — for example, **WillChangeRecordset** or **WillConnect**. Events that are called after an event has been completed usually include "Complete" in their names — for example, **RecordChangeComplete** or **ConnectComplete**. Exceptions exist — such as **InfoMessage** — but these occur after the associated operation has completed.

## <a name="will-events"></a>Will-Ereignisse

Durch Ereignishandler, die vor dem Starten der Operation aufgerufen werden, haben Sie Gelegenheit, die Operationsparameter zu untersuchen oder zu ändern und dann die Operation abzubrechen oder ihren Abschluss zuzulassen. Diese Ereignishandlerroutinen weisen in der Regel Namen des Formulars **Will* Event* auf.

## <a name="complete-events"></a>Complete-Ereignisse

Event handlers called after an operation completes can notify your application that an operation has concluded. Such an event handler is also notified when a Will event handler cancels a pending operation. Diese Ereignishandlerroutinen weisen in der Regel Namen des Formulars ***Event*Complete** auf.

Will- und Complete-Ereignisse werden normalerweise paarweise verwendet.

## <a name="other-events"></a>Andere Ereignisse

Die anderen Ereignishandler – d. h. Ereignisse, deren Namen nicht dem Format **Will*Event*** oder _Event_Complete entsprechen **–** werden erst nach Abschluss eines Vorgangs aufgerufen. Es handelt sich dabei um die Ereignisse **Disconnect**, **EndOfRecordset** und **InfoMessage**.

