---
title: Ereignistypen (Access-Desktop-Daten Bankreferenz)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3bcf631ffc6c9b4b847af3f973114d6b271d26f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314154"
---
# <a name="types-of-events"></a>Typen von Ereignissen


**Gilt für**: Access 2013, Office 2013



There are two basic types of events. "Will Events," which are called before an operation starts, usually include "Will" in their names — for example, **WillChangeRecordset** or **WillConnect**. Events that are called after an event has been completed usually include "Complete" in their names — for example, **RecordChangeComplete** or **ConnectComplete**. Exceptions exist — such as **InfoMessage** — but these occur after the associated operation has completed.

## <a name="will-events"></a>Will-Ereignisse

Durch Ereignishandler, die vor dem Starten der Operation aufgerufen werden, haben Sie Gelegenheit, die Operationsparameter zu untersuchen oder zu ändern und dann die Operation abzubrechen oder ihren Abschluss zuzulassen. Diese Ereignishandler-Routinen haben in der Regelnamen des Formulars **wird*Ereignis * * *.

## <a name="complete-events"></a>Complete-Ereignisse

Event handlers called after an operation completes can notify your application that an operation has concluded. Such an event handler is also notified when a Will event handler cancels a pending operation. Diese Ereignishandler-Routinen weisen in der Regel die Namen des Formulars ***Event * Complete**auf.

Will- und Complete-Ereignisse werden normalerweise paarweise verwendet.

## <a name="other-events"></a>Andere Ereignisse

Die anderen Ereignishandler, d. h. Ereignisse, deren Namen nicht das Formular sind, *** Ereignis*** oder ***Ereignis * vollständig-** werden erst aufgerufen, nachdem ein Vorgang abgeschlossen wurde. Es handelt sich dabei um die Ereignisse **Disconnect**, **EndOfRecordset** und **InfoMessage**.

