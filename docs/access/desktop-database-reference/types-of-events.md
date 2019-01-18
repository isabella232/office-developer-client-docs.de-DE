---
title: Arten von Ereignissen (Access PC-Datenbank-Referenz)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3bcf631ffc6c9b4b847af3f973114d6b271d26f5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718140"
---
# <a name="types-of-events"></a>Typen von Ereignissen


**Betrifft**: Access 2013, Office 2013



Es gibt zwei Basisereignistypen. Will-Ereignisse, die vor dem Starten einer Operation aufgerufen werden, enthalten normalerweise "Will" im Namen - z. B. WillChangeRecordset oder WillConnect. Ereignisse, die nach Abschluss eines Ereignisses aufgerufen werden, enthalten normalerweise "Complete" im Namen - z. B. RecordChangeComplete oder ConnectComplete. Es sind Ausnahmen vorhanden - z. B. InfoMessage -, diese treten jedoch nach Abschluss der zugeordneten Operation auf.

## <a name="will-events"></a>Will-Ereignisse

Durch Ereignishandler, die vor dem Starten der Operation aufgerufen werden, haben Sie Gelegenheit, die Operationsparameter zu untersuchen oder zu ändern und dann die Operation abzubrechen oder ihren Abschluss zuzulassen. Diese Ereignishandler-Routine verfügen normalerweise Namen des Formulars **werden*-Ereignis ***.

## <a name="complete-events"></a>Complete-Ereignisse

Ereignishandler wird aufgerufen, nachdem ein Vorgang abgeschlossen ist, können die Anwendung benachrichtigt, die eine Operation abgeschlossen wurde. Ein solcher Ereignishandler wird auch benachrichtigt, wenn ein Ereignishandler wird eine ausstehende Operation abbricht. Diese Ereignishandler-Routine verfügen normalerweise Namen des Formulars ***Ereignis * vollständig**.

Will- und Complete-Ereignisse werden normalerweise paarweise verwendet.

## <a name="other-events"></a>Andere Ereignisse

Die anderen Ereignishandler – d. h., Ereignisse, deren Namen nicht des Formulars **wird * Ereignis*** oder ***Ereignis * Complete –** sind nur nach Abschluss einer Operation aufgerufen. Diese Ereignisse sind **Trennen**, **EndOfRecordset**und **InfoMessage**.

