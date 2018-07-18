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
description: Bewirkt, dass die Anwendung ein Markerereignis für das Add-on, Microsoft Visual Basic für Applikationen (VBA)-Code oder COM-add-in auslöst.
ms.openlocfilehash: b9175caf0845530c93f6db15e286f3eae21ea415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797757"
---
# <a name="queuemarkerevent-function"></a>QUEUEMARKEREVENT Function

Bewirkt, dass die Anwendung ein Markerereignis für das Add-on, Microsoft Visual Basic für Applikationen (VBA)-Code oder COM-add-in auslöst. 
  
## <a name="syntax"></a>Syntax

QUEUEMARKEREVENT (** *Zeichenfolge Event_string* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Zeichenfolge event_string_ <br/> |Erforderlich  <br/> |**String** <br/> | Die Zeichenfolge, die an den Ereignishandler übergeben.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die QUEUEMARKEREVENT-Funktion bietet Entwicklern eine Möglichkeit Codeprobleme aus einer ShapeSheet-Zelle zu benachrichtigen und lösungsspezifische Informationen übergeben. Wenn die Zelle mit der Formel mit der QUEUEMARKEREVENT-Funktion ausgewertet wird, wird die Anwendung ein Markerereignis löst und übergibt die _Zeichenfolge Event_string_ an alle Ereignishandler, die auf das **MarkerEvent** -Ereignis warten. 
  
Weitere Informationen zu Markerereignissen finden Sie unter **QueueMarkerEvent** -Methode und **MarkerEvent** -Ereignis Themen in der Microsoft Visio Automation Reference. 
  
## <a name="example"></a>Beispiel

QUEUEMARKEREVENT ("MyCustomNotification") 
  
Bewirkt, dass die Anwendung ein Markerereignis auslöst und die Zeichenfolge "MyCustomNotification" an die Ereignishandler übergibt, die auf das **MarkerEvent**-Ereignis warten. 
  

