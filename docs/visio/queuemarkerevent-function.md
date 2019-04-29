---
title: QUEUEMARKEREVENT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60107
localization_priority: Normal
ms.assetid: b4671715-4209-7774-c174-c19dc9721a02
description: Bewirkt, dass die Anwendung ein Marker-Ereignis für Ihr Add-on, Microsoft Visual Basic für Applikationen (VBA)-Code oder ein COM-Add-in auslöst.
ms.openlocfilehash: 841f6acc63497a6f0b8930c89534b5f8b04c0393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418806"
---
# <a name="queuemarkerevent-function"></a>QUEUEMARKEREVENT Function

Bewirkt, dass die Anwendung ein Marker-Ereignis für Ihr Add-on, Microsoft Visual Basic für Applikationen (VBA)-Code oder ein COM-Add-in auslöst. 
  
## <a name="syntax"></a>Syntax

QUEUEMARKEREVENT (* * *event_string* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _event_string_ <br/> |Erforderlich  <br/> |**String** <br/> | Die an den Ereignishandler zu übergebende Zeichenfolge.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die QUEUEMARKEREVENT-Funktion bietet Entwicklern die Möglichkeit, ihren Code über eine ShapeSheet-Zelle zu benachrichtigen und lösungsspezifische Informationen zu übergeben. Wenn die Zelle mit der Formel mit der QUEUEMARKEREVENT-Funktion ausgewertet wird, löst die Anwendung ein Marker-Ereignis und übergibt _event_string_ an alle Ereignishandler, die das **MarkerEvent** -Ereignis überwachen. 
  
Weitere Informationen zu Marker-Ereignissen finden Sie unter den Themen **QueueMarkerEvent** -Methode und **MarkerEvent** -Ereignis in der Microsoft Visio-Automatisierungsreferenz. 
  
## <a name="example"></a>Beispiel

QUEUEMARKEREVENT ("MyCustomNotification") 
  
Bewirkt, dass die Anwendung ein Markerereignis auslöst und die Zeichenfolge "MyCustomNotification" an die Ereignishandler übergibt, die auf das **MarkerEvent**-Ereignis warten. 
  

