---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: Neuzuordnen von Terminen in einem Kalenderordner unterstützt.
ms.openlocfilehash: 57ca59121f74c7b64a84282c7493e4aed3179f7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791115"
---
# <a name="iolkapptrebaser"></a>IOlkApptRebaser

Neuzuordnen von Terminen in einem Kalenderordner unterstützt.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt:  <br/> |**IUnknown** <br/> |
|Headerdatei  <br/> |tzmovelib.h  <br/> |
|Implementiert von:  <br/> |tzmovelib.dll  <br/> |
|Aufgerufen von:  <br/> |MAPI-Clientanwendungen  <br/> |
|Eingeblendet auf:  <br/> |Basisadressen Outlook-Objekt  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)** <br/> |Beginnt eine Aufgabe für die Enumeration der Termin im Kalenderordner Termine zu finden, die neuen Basisadressen benötigen.  <br/> |
|**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)** <br/> |Termin-Enumeration in einem Kalenderordner Abschluss wartet, und gibt einer Liste von Terminen, müssen neuen Basisadressen.  <br/> |
|**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)** <br/> |Beginnt mit einer Aufgabe zum Termin Neuzuordnen anhand einer Liste von Terminen, in der Regel von **EndEnumerateAppointments**abgerufen.  <br/> |
|**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)** <br/> |Führen Sie neuen Basisadressen Termin wartet, und ruft die Ergebnisse ab.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

