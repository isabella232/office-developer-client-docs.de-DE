---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: Unterstützt das Neubasieren von Terminen in einem Kalenderordner.
ms.openlocfilehash: cf4f7c790a8561f149160c83418a0d5ebd91a455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410070"
---
# <a name="iolkapptrebaser"></a>IOlkApptRebaser

Unterstützt das Neubasieren von Terminen in einem Kalenderordner.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt von:  <br/> |**IUnknown** <br/> |
|Headerdatei  <br/> |tzmovelib.h  <br/> |
|Implementiert von:  <br/> |tzmovelib.dll  <br/> |
|Aufgerufen von:  <br/> |MAPI-Clientanwendungen  <br/> |
|Verfügbar gemacht für:  <br/> |Outlook-Neubasierungsobjekt  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)** <br/> |Beginnt eine Aufgabe für die Enumeration der Termin im Kalenderordner Termine zu finden, die neuen Basisadressen benötigen.  <br/> |
|**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)** <br/> |Termin-Enumeration in einem Kalenderordner Abschluss wartet, und gibt einer Liste von Terminen, müssen neuen Basisadressen.  <br/> |
|**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)** <br/> |Beginnt eine Aufgabe für die Terminumbasierung mit einer Liste von Terminen, die in der Regel von **EndEnumerateAppointments erhalten werden.**  <br/> |
|**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)** <br/> |Führen Sie neuen Basisadressen Termin wartet, und ruft die Ergebnisse ab.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

